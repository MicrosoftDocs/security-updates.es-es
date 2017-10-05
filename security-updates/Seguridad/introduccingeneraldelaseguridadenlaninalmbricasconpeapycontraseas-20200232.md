---
TOCTitle: Introducción general de la seguridad en LAN inalámbricas con PEAP y contraseñas
Title: Introducción general de la seguridad en LAN inalámbricas con PEAP y contraseñas
ms:assetid: '849829a4-3247-48cc-81c7-131647c45328'
ms:contentKeyID: 20200232
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd162271(v=TechNet.10)'
---

Seguridad en LAN inalámbricas con PEAP y contraseñas
====================================================

### Introducción general de la seguridad en LAN inalámbricas con PEAP y contraseñas

Actualizado: agosto 25, 2004

[Ver todos los temas de la guía de seguridad](http://technet.microsoft.com/es-es/security/bb977553.aspx)

##### En esta página

[](#edaa)[Introducción](#edaa)
[](#ecaa)[Información general de la solución](#ecaa)
[](#nlsw)[Capítulo 1: Seguridad en LAN inalámbricas con PEAP y contraseñas](#nlsw)
[](#npsw)[Capítulo 2: Planeamiento de la implementación de seguridad en LAN inalámbricas](#npsw)
[](#apsw)[Capítulo 3: Preparación del entorno](#apsw)
[](#adsw)[Capítulo 4: Creación de la entidad emisora de certificados de red](#adsw)
[](#adse)[Capítulo 5: Creación de la infraestructura de seguridad de LAN inalámbricas](#adse)
[](#acse)[Capítulo 6: Configuración de clientes de LAN inalámbricas](#acse)
[](#zcse)[Capítulo 7: Prueba de soluciones de seguridad en LAN inalámbricas](#zcse)
[](#mase)[Capítulo 8: Mantenimiento de soluciones de seguridad en LAN inalámbricas](#mase)
[](#maza)[Apéndice A: Uso de PEAP en la empresa](#maza)
[](#mazx)[Apéndice B: Uso de WPA en la solución](#mazx)
[](#mazy)[Apéndice C: Versiones de sistemas operativos compatibles](#mazy)
[](#mazr)[Apéndice D: Secuencias de comandos y archivos auxiliares](#mazr)
[](#maur)[Introducción: Elección de una estrategia para la seguridad en LAN inalámbricas](#maur)

### Introducción

*Seguridad en LAN inalámbricas con PEAP y contraseñas* es la segunda guía de soluciones de seguridad para WLAN de Microsoft®. Esta solución está diseñada para guiarle a través del ciclo completo de planeamiento, implementación, prueba y administración de soluciones de seguridad inalámbricas. Se sirve de una arquitectura flexible que se adapta tanto a aquellas organizaciones con menos de 50 usuarios, como a las que cuentan con varios miles. La solución se basa en el protocolo de autenticación 802.1x del Instituto de ingenieros de electricidad y electrónica (IEEE). Se creó y probó en clientes Microsoft® Windows® XP, clientes Microsoft Pocket PC 2003, y en equipos que ejecutan Microsoft Windows Server™ 2003.

Esta guía de soluciones es complementaria a la primera solución de seguridad para WLAN de Microsoft, "[Solución de Seguridad de LAN inalámbricas — Servicios de Certificate Server de Microsoft Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14843)". Mientras que la primera solución estaba dirigida a grandes organizaciones, ésta es más sencilla y está diseñada para que organizaciones pequeñas y medianas puedan implementarla fácilmente. Una de las principales diferencias de la solución *Seguridad en LAN inalámbricas con PEAP y contraseñas* es que utiliza nombres de usuario y contraseñas para autenticar el acceso de usuarios y equipos a la red WLAN, en lugar de recurrir a los certificados digitales utilizados en la primera solución. Otra característica distintiva de esta solución es el uso de hardware del servidor existente (en lugar de necesitar nuevas adquisiciones), de un modelo de administración más sencillo y de secuencias de comandos y configuraciones predefinidas. De esta forma, se automatizan muchas más tareas de configuración que en la solución anterior.

Esta guía presenta dos características significativas que la distinguen de la documentación de productos de Windows® y de muchas notas técnicas del producto disponibles en Microsoft. En primer lugar, esta guía se basa en instrucciones sobre la *solución* más que sobre el producto. Es una guía que se centra en proporcionar una infraestructura de seguridad para LAN inalámbricas, más que en describir los detalles de funcionalidad del producto. Esta guía comprende una solución *integral* que engloba el ciclo completo de planeamiento, creación, prueba y administración de la solución. En segundo lugar, es una guía de carácter *normativo*; las opciones de diseño de la solución se basaron en prácticas recomendadas y conocimientos obtenidos de las implementaciones de WLAN en Microsoft y sus clientes. La solución descrita en la guía se creó y probó en laboratorios de Microsoft para garantizar que su funcionamiento era el esperado.

[](#mainsection)[Principio de la página](#mainsection)

### Información general de la solución

Esta guía se divide en cuatro secciones, cada una de las cuales corresponde a una fase del ciclo de la solución, que incluye el planeamiento, la implementación, la prueba y el funcionamiento.

[![](images/Dd162271.PEAP_001(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_001_big(es-es,technet.10).gif)

**Figura 1.1. Información general de la solución para la seguridad en LAN inalámbricas con PEAP y contraseñas**

La sección sobre planeamiento consiste en una introducción, "Elección de una estrategia para la seguridad en LAN inalámbricas" y el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas". Los cuatro capítulos siguientes constituyen la sección de la guía dedicada a la creación e implementación. Estos capítulos ofrecen instrucciones para implementar los servidores del Servicio de usuario de acceso telefónico de autenticación remota (RADIUS) utilizando el Servicio de autenticación de Internet (IAS) de Windows Server 2003, así como para implementar los clientes inalámbricos y la infraestructura compatible. Cada capítulo proporciona procedimientos detallados sobre la instalación y configuración de los componentes de software y sobre cómo integrarlos en una solución que pueda usar en su organización. También incluyen procedimientos de comprobación para ayudar a minimizar errores.

La sección dedicada a la prueba cubre un capítulo que explica cómo comprobar que la solución funciona correctamente antes de su implementación. El mantenimiento de la solución viene reflejado en un capítulo que explica cómo manejar, supervisar y modificar todos los componentes de la solución, y cómo solucionar los problemas de éstos.

Por último, la guía viene acompañada de un conjunto de herramientas y secuencias de comandos que puede utilizar para automatizar muchas de las tareas de implementación y funcionamiento.

[](#mainsection)[Principio de la página](#mainsection)

#### Soporte técnico

Para obtener más información sobre el soporte técnico de los productos Microsoft de esta solución, que incluye niveles superiores de notificación, ofertas de soporte técnico, recursos y niveles de compatibilidad, consulte <http://support.microsoft.com/>.

#### Descargas y recursos

Descargue la solución en [http://go.microsoft.com/fwlink/?LinkId=23481](http://go.microsoft.com/fwlink/?linkid=23481).

Puede que también encuentre útiles los siguientes recursos:

-   Para obtener más información sobre la seguridad en Microsoft, consulte la página sobre seguridad e informática de confianza para TI de Microsoft TechNet® en [http://www.microsoft.com/technet/security/Default.mspx](http://www.microsoft.com/technet/security/default.mspx).

-   Para obtener más información sobre Microsoft Windows Server™ 2003 y Wi-Fi, consulte la página sobre Wi Fi en el sitio Web de Windows Server System en <http://www.microsoft.com/wifi>.

-   Para obtener más información sobre los estándares inalámbricos del IEEE, consulte el sitio Web del IEEE en <http://standards.ieee.org/wireless/>.

-   Para obtener más información sobre Wi-Fi Alliance, consulte el sitio Web de la organización en <http://www.wi-fialliance.org/>.

#### Envíenos sus comentarios

Microsoft está interesado en sus comentarios sobre este material. Sobre todo, no dude en enviarnos su opinión sobre los siguientes temas:

-   Utilidad de la información proporcionada

-   Precisión de los procedimientos descritos paso a paso

-   Facilidad de lectura y grado de interés de los capítulos

-   Valoración general de la solución

Envíe sus comentarios a la siguiente dirección de correo electrónico: [SecWish@Microsoft.com.](mailto:secwish@microsoft.com?subject=feedback%20re:%20microsoft%20solution%20for%20securing%20wireless%20lans%20with%20peap%20and%20passwords)

#### Créditos

**Autor:** Ian Hellen

**Administración del programa:** Bruce Lobree, Karl Grunwald, Jeff Coon

**Prueba:** Mehul Mediwala

**Coautor:** Stirling Goetz

**Edición:** Vidyatech

**Revisores:** Drew Baron, David Cross, Joseph Davies, Stirling Goetz, Mike Greer, Jesper Johansson, Carsten Kinder, Ashwin Palekar, Steve Riley (SBU), Ray Sun, Laudon Williams, Shain Wray

(Este artículo contiene referencias a guías de otros productos y vínculos a sitios Web que sólo están disponibles en inglés.)

[](#mainsection)[Principio de la página](#mainsection)

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 1: Seguridad en LAN inalámbricas con PEAP y contraseñas

[](#aeaa)[Introducción](#aeaa)
[](#adaa)[Información general de la solución](#adaa)
[](#acaa)[Convenciones de estilo](#acaa)
[](#abaa)[Soporte técnico y comentarios](#abaa)

### Introducción

Hoy en día, la tecnología inalámbrica es un tema de debate de gran actualidad en el mundo empresarial. La mayoría de las organizaciones ya han implementado redes de área local inalámbricas (WLAN) o están en plena discusión sobre las ventajas e inconvenientes de esta tecnología. Son innegables las mejoras en productividad percibidas por los usuarios y el atractivo que suponen las redes de bajo mantenimiento para los departamentos de tecnología de la información (TI). No obstante, la gran preocupación por la seguridad de la mayoría de los directores de TI ha hecho que reaccionen con prudencia, si no con rotunda hostilidad, ante la idea de introducir redes WLAN en las organizaciones. Al mismo tiempo, la implementación de las soluciones propuestas por los analistas y proveedores de redes para afrontar estas preocupaciones ha parecido demasiado compleja y costosa.

*Seguridad en LAN inalámbricas con PEAP y contraseñas* es la segunda solución de seguridad para WLAN de Microsoft®. Es un complemento de la primera solución, *Solución de Seguridad de LAN inalámbricas — Servicios de Certificate Server de Microsoft Windows Server 2003*. Mientras que la primera solución estaba dirigida a grandes organizaciones, ésta es considerablemente más sencilla, más fácil de implementar y está diseñada para organizaciones pequeñas y medianas. La primera diferencia tecnológica entre las dos soluciones es que la primera utiliza certificados con clave pública para autenticar el acceso de usuarios y equipos a WLAN, mientras que la segunda utiliza nombres de usuario y contraseñas. Otra característica distintiva de esta solución es el uso de hardware existente del servidor (en lugar de utilizar hardware nuevo), el empleo de un modelo de delegación administrativa más sencillo y la automatización de muchas más tareas de configuración mediante secuencias de comandos y configuraciones predefinidas.

La documentación de esta solución presenta dos características significativas que la distinguen de la documentación general de productos del sistema operativo Microsoft Windows® y de muchas notas técnicas del producto de Microsoft. La primera es la naturaleza *normativa* de la guía, en la que las opciones de diseño estaban disponibles y las decisiones se tomaron en base a los conocimientos obtenidos a partir de la implementación interna y los comentarios de los clientes recibidos por Microsoft. La solución se basó en estas prácticas recomendadas y se creó y probó en los laboratorios de Microsoft para garantizar que el funcionamiento de la solución era el esperado. La segunda característica es que se trata de una solución *integral* que engloba el ciclo completo de diseño, planeamiento, creación, prueba y administración de la solución.

Como se detallará en los capítulos siguientes, la solución se basa en el estándar 802.1X del Instituto de ingenieros de electricidad y electrónica (IEEE) y requiere una infraestructura RADIUS (Servicio de usuario de acceso telefónico de autenticación remota). Se sirve de una arquitectura flexible que se puede adaptar tanto a organizaciones con decenas de usuarios, como a aquéllas con miles de ellos. La solución se creó y probó en equipos cliente con Microsoft Windows® XP, con Microsoft Pocket PC 2003 y en servidores con Microsoft Windows Server™ 2003.

[](#mainsection)[Principio de la página](#mainsection)

### Información general de la solución

Esta guía se divide en cuatro secciones, cada una de la cuales corresponde a una fase del ciclo de la solución. Estas fases son el planteamiento, la implementación, la prueba y el funcionamiento. Dichas fases se vuelven a dividir en capítulos.

[![](images/Dd162271.PEAP_101(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_101_big(es-es,technet.10).gif)

**Figura 1.1. Información general de Seguridad en LAN inalámbricas**

La sección de planeamiento consiste en una introducción, "Elección de una estrategia para la seguridad en LAN inalámbricas" y el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas". Los cuatro capítulos siguientes constituyen la sección de la guía dedicada a la creación e implementación. Estos capítulos ofrecen instrucciones para implementar los servidores RADIUS utilizando el Servicio de autenticación de Internet (IAS) de Windows Server 2003, así como para implementar los equipos clientes inalámbricos y la infraestructura compatible. Cada capítulo ofrece procedimientos detallados sobre la instalación y configuración de los componentes de software, y sobre el modo de integrarlos en la solución. También incluyen procedimientos de comprobación que ayudan a minimizar errores.

La sección dedicada a la prueba cubre un capítulo que explica cómo confirmar que la solución funciona correctamente antes de su implementación. La sección sobre el funcionamiento ocupa también un único capítulo. Éste explica cómo manejar, supervisar y modificar todos los componentes de la solución, y cómo solucionar los problemas de éstos.

La guía viene acompañada de un conjunto de herramientas y de secuencias de comandos utilizadas para automatizar muchas de las tareas de implementación y funcionamiento.

La siguiente sección ofrece una descripción más detallada de cada capítulo.

### Elección de una estrategia para la seguridad en LAN inalámbricas

Este documento sirve de introducción a las dos soluciones de seguridad en WLAN descritas anteriormente. Su objetivo es ayudarle a seleccionar la estrategia adecuada para la infraestructura de seguridad de la red inalámbrica. Describe las razones empresariales que conducen a la adopción de la tecnología WLAN y las preocupaciones sobre la seguridad que la rodean. Trata las diferentes opciones disponibles para abordar estas preocupaciones y destaca una solución basada en la autenticación segura y en la protección de los datos de red. Del mismo modo, contiene un análisis sobre los méritos relativos de los diferentes enfoques sobre seguridad en WLAN, incluidas las soluciones originarias de seguridad en WLAN, las redes privadas virtuales (VPN) y la seguridad IP.

### Capítulo 1: Seguridad en LAN inalámbricas con PEAP y contraseñas

Este capítulo es el que nos ocupa y proporciona información general sobre el contenido de la guía de la solución.

### Capítulo 2: Planeamiento de la implementación de seguridad en LAN inalámbricas

Este capítulo describe el diseño de la arquitectura de la solución de seguridad en LAN inalámbricas. Cubre los siguientes temas:

-   Funcionamiento de una solución basada en el protocolo 802.1X y en el Protocolo de autenticación extensible protegido (PEAP).

-   Descripción de la organización de destino para esta solución y los criterios de diseño clave de la solución.

-   Desarrollo de un diseño de la solución de seguridad en WLAN según las necesidades de la organización de destino.

-   Adaptación del diseño básico a organizaciones de mayor tamaño.

-   Análisis de las variaciones del diseño para ajustarse a las necesidades que no se encuentran en la solución, como la introducción de VPN o de redes 802.1X con cable.

El capítulo se centra en el diseño de una infraestructura RADIUS (utilizando IAS, la implementación RADIUS incluida en Windows Server) para proporcionar una autenticación segura y servicios de administración clave. El capítulo incluye además un análisis de los equipos cliente inalámbricos compatibles con la solución y con los requisitos de certificados.

### Capítulo 3: Preparación del entorno

Este capítulo se ocupa de la tecnología de la información (TI) subyacente necesaria para admitir esta solución de WLAN. Describe la preparación del directorio activo de Microsoft Active Directory®, el Protocolo de configuración dinámica de host (DHCP), los servicios del Sistema de nombres de dominio (DNS) y los requisitos de redes subyacentes. Además incluye una serie de procedimientos para aplicar las configuraciones de seguridad y para instalar las actualizaciones de seguridad necesarias en los servidores utilizados en la solución.

### Capítulo 4: Creación de la entidad emisora de certificados de red

Este capítulo describe cómo instalar una sencilla entidad emisora de certificados en un controlador de dominio con el objetivo de proporcionar certificados a los servidores IAS. Los procedimientos para su consecución se automatizan en gran parte mediante secuencias de comandos incluidas en la guía. La entidad emisora creada para esta solución se dedica a la tarea específica de emitir certificados para los servidores IAS y, en consecuencia, requiere un mantenimiento escaso o periódico.

### Capítulo 5: Creación de la infraestructura de seguridad en LAN inalámbricas

Este capítulo ofrece instrucciones sobre la implementación de los componentes de seguridad en WLAN, los servidores IAS y los puntos de acceso inalámbricos. Incluye instrucciones paso a paso sobre cómo instalar IAS en un controlador de dominio (o servidor miembro), cómo establecer la configuración y las directivas de IAS, cómo instalar puntos de acceso inalámbricos para utilizar los servidores IAS y cómo replicar la configuración de IAS entre los servidores IAS.

### Capítulo 6: Configuración de clientes de LAN inalámbricas

Este capítulo contiene los procedimientos necesarios para configurar los clientes compatibles con esta solución. Las tres secciones principales del capítulo se centran en el control del acceso de usuarios y equipos a la WLAN, la configuración de las directivas de grupo para clientes WLAN en Windows XP y la configuración manual de WLAN para los clientes Pocket PC 2003.

### Capítulo 7: Prueba de soluciones de seguridad en LAN inalámbricas

Este capítulo es el resultado del plan de prueba utilizado por el equipo de Microsoft al probar esta solución. Los capítulos dedicados a la creación (3-6) contienen procedimientos de comprobación habituales utilizados en todo el proceso de creación para comprobar que todo avanzaba correctamente. Este capítulo complementa aquellos procedimientos con un conjunto de pruebas adicionales que debería llevar a cabo antes de implementar la solución en producción.

### Capítulo 8: Mantenimiento de soluciones de seguridad en LAN inalámbricas

Este capítulo se centra en mantener el funcionamiento adecuado de la infraestructura de seguridad en la WLAN. La primera parte del capítulo incluye las tareas operativas clave que necesita para mantener el sistema. Se dividen en diferentes categorías que abarcan lo siguiente: tareas de mantenimiento diario, supervisión y alertas; introducción de modificaciones en el entorno, optimización del rendimiento y solución de problemas. La sección final sobre solución de problemas contiene una serie de diagramas de flujo, tablas y procedimientos, descripciones detalladas de herramientas y técnicas para la solución de problemas que puede utilizar en el diagnóstico y resolución de éstos.

### Apéndices

##### Apéndice A: Uso de PEAP en la empresa

Esta solución se diseñó para pequeñas y medianas empresas. Esto contrasta con la solución de WLAN basada en certificados (mencionada anteriormente) que se diseñó para organizaciones de nivel empresarial. No obstante, una solución de WLAN que utilice PEAP y contraseñas también se puede utilizar en organizaciones de gran tamaño.

Este apéndice muestra cómo puede adaptar la información sobre la solución de WLAN basada en certificados y orientada a la empresa, con el objetivo de implementar una solución de WLAN basada en PEAP y contraseñas.

##### Apéndice B: Uso de WPA en la solución

Este apéndice facilita información sobre el estado de compatibilidad con la seguridad en el Acceso protegido WiFi (WPA) y sobre cómo puede utilizar la protección de datos mediante WPA en lugar de WEP (Privacidad equivalente por cable) dinámica. Esta solución se diseñó para admitir WPA, el cual se menciona a lo largo de esta guía. No obstante, cuando la solución se estaba desarrollando, la compatibilidad con WPA no era aún universal y, por tanto, no se utilizó como opción predeterminada.

##### Apéndice C: Versiones de sistemas operativos compatibles

Este apéndice consta de una tabla en la que se muestran las versiones de sistemas operativos en esta solución compatibles con clientes inalámbricos y con varias funciones de servidor. Su finalidad es responder a las dudas sobre la posibilidad de utilizar versiones alternativas de Windows y de otras plataformas en las diversas funciones de esta solución.

##### Apéndice D: Secuencias de comandos y archivos auxiliares

Los procedimientos descritos en los capítulos dedicados a la implementación y funcionamiento utilizan una serie de secuencias de comandos y otros archivos auxiliares. Este apéndice describe las secuencias de comandos y su funcionamiento. Esta información también aparece en el archivo SecuringWirelessLANs.rtf incluido con las secuencias de comandos.

[](#mainsection)[Principio de la página](#mainsection)

### Convenciones de estilo

La siguiente tabla describe las convenciones de estilo utilizadas en la guía.

**Tabla 1.1. Convenciones de estilo**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Elemento</th>
<th style="border:1px solid black;" >Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Negrita</strong></td>
<td style="border:1px solid black;">Caracteres que se escriben exactamente tal y como se muestran, incluidos comandos y modificadores. Los elementos de la interfaz de usuario (UI) que aparecen en el texto con carácter normativo también se muestran en negrita.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><em>Cursiva</em></td>
<td style="border:1px solid black;">La cursiva se utiliza en dos contextos especiales:
—Si la cursiva aparece en el cuerpo principal del texto, indica que se trata del título de otro documento.
—Si la cursiva aparece en comandos o códigos (o en texto que haga referencia a un comando o código), indica que se trata de marcadores de posición para variables donde se han de insertar valores específicos. Por ejemplo, <em>nombreDeArchivo.ext</em> indica que debe sustituir el texto en cursiva <em>nombreDeArchivo.ext</em> con el nombre de archivo de su elección.
La cursiva también se utiliza en ocasiones para enfatizar texto normal.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Texto en pantalla</td>
<td style="border:1px solid black;">Para el texto visualizado en pantalla (por ejemplo, los resultados de una herramienta de línea de comandos) y para comandos que hay que escribir en la línea de comandos.
Algunos comandos no se ajustan a los márgenes de la página. Cuando sucede esto, el texto del comando se divide en varias líneas con las líneas posteriores con sangría (indicado en una nota a continuación del comando).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Fuente monoespaciada</td>
<td style="border:1px solid black;">Ejemplos de código y contenidos de archivos de configuración.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">%SystemRoot%</td>
<td style="border:1px solid black;">Carpeta en la que se instala el sistema operativo Windows Server 2003.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Nota</strong></td>
<td style="border:1px solid black;">Avisa al lector de la existencia de información adicional.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Importante</strong></td>
<td style="border:1px solid black;">Avisa al lector de la existencia de información adicional esencial para finalizar la tarea.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Precaución</strong></td>
<td style="border:1px solid black;">Avisa al lector de que el incumplimiento u omisión de una acción concreta puede producir pérdida de datos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Advertencia</strong></td>
<td style="border:1px solid black;">Avisa al lector de la situación en la que el incumplimiento u omisión de una acción concreta puede producir lesiones físicas al usuario o daños al hardware.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Soporte técnico y comentarios
  
### Soporte técnico
  
Para obtener más ayuda sobre la implementación de las tecnologías tratadas en esta solución, póngase en contacto con la oficina de Microsoft de su zona o con una empresa asociada a los servicios de Microsoft.
  
-   Para encontrar la oficina de Microsoft de su zona, visite la siguiente dirección URL y seleccione el país y región pertinente
  
    <http://www.microsoft.com/worldwide/>.
  
-   Para obtener más información sobre el soporte técnico de los componentes de Windows Server 2003 utilizados en esta solución, que incluye niveles superiores de notificación, ofertas de soporte técnico, recursos y niveles de soporte técnico, consulte la siguiente dirección URL:
  
    [http://support.microsoft.com](http://support.microsoft.com/).
  
### Envíenos sus comentarios
  
Microsoft está interesado en sus comentarios sobre este material. Sobre todo, no dude en enviarnos su opinión sobre los siguientes temas:
  
-   Utilidad de la información proporcionada
  
-   Precisión de los procedimientos descritos paso a paso
  
-   Facilidad de lectura y grado de interés de los capítulos
  
-   Valoración general de la solución
  
Envíe sus comentarios a la siguiente dirección de correo electrónico: [SecWish@Microsoft.com](mailto:secwish@microsoft.com?subject=feedback%20re:%20microsoft%20solution%20for%20secure%20wireless%20lans).
  
(Este artículo contiene referencias a guías de otros productos y vínculos a sitios Web que sólo están disponibles en inglés.)
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 2: Planeamiento de la implementación de seguridad en LAN inalámbricas
  
[](#ekaa1)[Información general](#ekaa1)  
[](#ejaa1)[Requisitos previos del capítulo](#ejaa1)  
[](#eiaa1)[Modo de funcionamiento de la seguridad de LAN inalámbrica](#eiaa1)  
[](#ehaa1)[Perfil de la organización de destino](#ehaa1)  
[](#egaa1)[Criterios de diseño](#egaa1)  
[](#efaa1)[Arquitectura de WLAN](#efaa1)  
[](#eeaa1)[Escalabilidad para organizaciones más grandes](#eeaa1)  
[](#edaa1)[Variaciones en la arquitectura de la solución](#edaa1)  
[](#ecaa1)[Resumen](#ecaa1)  
[](#ebaa1)[Referencias](#ebaa1)
  
### Información general
  
El objetivo de este capítulo, que trata las pautas generales de diseño de la solución de red de área local inalámbrica (WLAN) segura, reside en describir minuciosamente el diseño de la solución y las razones para hacerlo de tal forma. Asimismo, proporciona toda la información precisa para adaptar el diseño a las necesidades particulares de la organización.
  
El capítulo comienza con una descripción del funcionamiento de 802.1X y del protocolo de autenticación extensible (PEAP) para proteger el acceso a la red. A continuación, se especifica la organización de destino de la solución, al tiempo que se explican algunos de los requisitos clave.
  
A mediados del capítulo se describe el diseño de la solución de WLAN, y así, aspectos como el diseño de la red; la situación del servidor del servicio de autenticación de Internet (IAS); la selección del hardware y del software; la obtención de certificados y la configuración del cliente. Del mismo modo, se indica cómo migrar de una WLAN sin protección a 802.1X y PEAP.
  
Las secciones que ponen fin al capítulo se centran en las variaciones que pueden darse en el diseño básico de la solución. El aspecto más importante de estas variaciones de diseño (que se trata en profundidad) es la forma en que la solución se escala para que pueda usarse en organizaciones más grandes. Otras opciones de diseño que se contemplan son:
  
-   Reutilización de la infraestructura de IAS para la seguridad de LAN con cable.
  
-   Utilización de IAS para la autenticación de acceso remoto.
  
-   Implementación de WLAN en entornos SOHO.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Requisitos previos del capítulo
  
Parte del planeamiento de la implementación de la WLAN segura consiste en garantizar que la organización posea las habilidades necesarias y que, asimismo, se implique a las personas adecuadas para que tomen las decisiones pertinentes relativas a la implementación.
  
Si desea sacar el máximo partido del capítulo, sería conveniente que se familiarizara con los siguientes temas:
  
-   Conceptos relacionados con la red, en concreto LAN inalámbricas.
  
-   Microsoft® 2000 Windows® o Windows Server™ 2003.
  
-   Conceptos del servicio de directorio Microsoft Active Directory®, incluidos los dominios y bosques de Active Directory, las herramientas de administración, el uso de la directiva de grupo y la manipulación de usuarios, grupos y otros objetos de Active Directory.
  
-   Conceptos de Servicios de Certificate Server e infraestructura de claves públicas.
  
-   Conceptos generales de seguridad como la autenticación, la autorización y el cifrado.
  
-   Características de seguridad de Windows como usuarios, grupos, auditorías y listas de control de acceso.
  
-   Aplicación de la configuración de seguridad mediante la directiva de grupo.
  
    **Nota:** si bien esta solución puede implementarse sin poseer un amplio conocimiento técnico, sería conveniente tener una certificación Microsoft Certified Systems Engineer (MSCE) o bien, conocimiento y experiencia equivalentes.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Modo de funcionamiento de la seguridad de LAN inalámbrica
  
En el documento de introducción ("Elección de una estrategia para la seguridad en LAN inalámbricas") se han tratado con detenimiento algunos de los métodos para proteger las WLAN, con especial atención al uso de la autenticación segura para WLAN a través de 802.1X y del cifrado del tráfico de red mediante la privacidad equivalente por cable (WEP) dinámica o el acceso protegido Wi-Fi (WPA). A continuación se señalan los puntos clave relacionados con este tema:
  
-   El esquema de seguridad de WLAN 802.11 original (conocido como WEP), contiene graves deficiencias de seguridad que posibilitan que un atacante descubra la clave de red para poder adentrarse en ella. Este esquema también se conoce como "WEP estática", debido a que emplea un acceso a red fijo y una clave de cifrado que todos los miembros de la WLAN comparten.
  
-   El uso de IEEE 802.1X proporciona un mecanismo de control de acceso seguro para la WLAN que ha de asociarse al mismo tiempo con un método de protocolo de autenticación extensible (EAP). La elección de este método de EAP define el tipo de credenciales que pueden usarse a la hora de autenticar usuarios y equipos en la WLAN.
  
-   Microsoft admite y recomienda el uso, por un lado, de PEAP con MS-CHAP v2 en el caso de la autenticación de contraseñas y, por otro, de EAP-TLS para la autenticación de certificados.
  
-   PEAP constituye un medio de protección de otro método de EAP (como pueda ser MS-CHAP v2) en el canal de seguridad. De este modo, PEAP se convierte en un elemento esencial para evitar ataques a métodos de EAP basados en contraseñas.
  
-   Una buena protección de datos del tráfico de WLAN puede conseguirse por medio tanto de una WEP dinámica como de una WPA. Las claves de cifrado maestras para la protección de datos se generan como parte del proceso de autenticación 802.1X (aunque la WEP dinámica y WPA emplean estas claves de manera distinta).
  
-   La distinción entre WEP estática y WEP dinámica es crucial, ya que ésta última emplea los mismos algoritmos de cifrado que la WEP estática, si bien actualiza las claves de cifrado de forma constante para acabar con ataques conocidos a la WEP estática. La WEP dinámica sólo hace referencia al mecanismo de protección de los datos de la red, en tanto que la autenticación de red se controla de forma separada mediante 802.1X.
  
#### Funcionamiento de 802.1X con PEAP y contraseñas
  
Microsoft admite el uso de PEAP con MS-CHAP v2 para la autenticación de la WLAN basada en contraseñas. La figura 2.2 ilustra el modo en que 802.1X con PEAP y MS-CHAP v2 funciona.
  
[![](images/Dd162271.PEAP_201(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_201_big(es-es,technet.10).gif)
  
**Figura 2.1. Autenticación 802.1X y PEAP para la LAN inalámbrica**
  
La figura muestra los siguientes cuatro componentes principales:
  
-   **Cliente inalámbrico:** se trata de un equipo o dispositivo que ejecuta una aplicación que requiere acceso a los recursos de red. El propietario de las credenciales que se usan para autenticar al cliente en la red puede ser tanto un usuario como un equipo. El cliente debe tener un adaptador de red WLAN que sea compatible con 802.1X y la WEP dinámica o con el cifrado de WPA. Este cliente, además, es conocido como estación (STA) en una gran cantidad de documentos sobre estándares de red.
  
    Antes de que el cliente pueda tener acceso a la WLAN, deberá ponerse de acuerdo con el servicio de autenticación (el servidor RADIUS y el directorio) en una serie de credenciales mediante una operación fuera de banda. En tal caso, las cuentas de dominio del usuario y del equipo se crean antes de que se produzca la conexión a WLAN. El cliente sabe la contraseña que le corresponde, mientras que el controlador de dominio (el directorio) puede comprobarla. Asimismo, el cliente ha de preconfigurarse con los valores de configuración de WLAN adecuados, que engloban el nombre WLAN y el método de autenticación que ha de utilizarse.
  
    **Nota:** en un sentido riguroso, sólo es preciso acordar (ya sea el usuario o el equipo) una serie de credenciales fuera de banda. Así, puede conectarse a la WLAN utilizando las credenciales de usuario para, a continuación, unir el equipo al dominio; no obstante, en esta solución se da por hecho que las cuentas de usuario y de equipo existían previamente al acceso a la WLAN.
  
-   **Punto de acceso inalámbrico:** el punto de acceso inalámbrico tiene como función el control del acceso a la WLAN y, al mismo tiempo, la unión de la conexión del cliente a la LAN interna. Debe ser compatible con 802.1X y la WEP dinámica o con el cifrado de WPA. En términos de conexión a red estándar, los puntos de acceso cumplen la función del Servicio de acceso a la red (NAS).
  
    Asimismo, el punto de acceso inalámbrico y el servidor RADIUS comparten un secreto que les permite identificarse mutuamente sin riesgo alguno.
  
-   **El servidor RADIUS y el directorio:** el servidor RADIUS utiliza el directorio para comprobar las credenciales de los clientes WLAN, al tiempo que toma decisiones relativas a la autorización en función de una directiva de acceso a red. También puede recopilar información de responsabilidad y de auditoría sobre el acceso de los clientes a la red. Esto se conoce como servicio de autenticación (AS) en términos de estándares de red.
  
-   **La red interna:** se trata de una red segura a la que la aplicación cliente inalámbrica debe obtener acceso.
  
Los siguientes pasos indican el modo en que el cliente realiza una solicitud y recibe permiso para tener acceso a la WLAN (y, en consecuencia, a la red interna). La numeración de estos pasos se corresponde con los números de la figura 2.1.
  
1.  Cuando el equipo cliente se encuentra dentro del alcance del punto de acceso inalámbrico, intenta conectarse a la WLAN que se encuentre activa en este punto y que el Identificador del conjunto de servicios (SSID) haya identificado. El SSID es el nombre de la WLAN que el cliente utiliza para identificar la configuración correcta y el tipo de credencial para esta WLAN en particular.
  
2.  El punto de acceso inalámbrico se configura con el propósito de permitir sólo conexiones seguras (autenticadas mediante 802.1X). Así, cuando el cliente intente conectarse al punto, éste le desafiará. A continuación, el punto de acceso configura un canal restringido que permite al cliente comunicarse únicamente con el servidor RADIUS (se bloquea el acceso al resto de la red). Por su parte, el servidor RADIUS sólo admitirá una conexión proveniente de un punto de acceso inalámbrico de confianza; es decir, una conexión que se haya configurado como un cliente RADIUS en el servidor IAS y que, por lo tanto, proporcione el secreto compartido para tal cliente RADIUS.
  
    El cliente intenta autenticarse en el servidor RADIUS a través del canal restringido por medio de 802.1X. Dentro de la negociación PEAP, el cliente establece una sesión de seguridad de la capa de transporte (TLS) con el servidor RADIUS. Una sesión TLS se utiliza como parte de los servidores PEAP con fines diversos:
  
    -   Permite que el cliente autentique el servidor RADIUS; esto significa que el cliente sólo establecerá la sesión con un servidor que cuente con un certificado en el que confíe el cliente.
  
    -   Protege el protocolo de autenticación MS-CHAP v2 frente al rastreo de paquetes.
  
    -   La negociación de la sesión TLS genera una clave que el cliente y el servidor RADIUS pueden utilizar a fin de establecer claves maestras comunes (que, a su vez, se usan para generar aquellas claves que van a emplearse para cifrar el tráfico de WLAN).
  
    Bajo la protección del canal de PEAP, el cliente se autentica en el servidor RADIUS utilizando el protocolo EAP MS-CHAP v2. En el transcurso de este intercambio, el tráfico dentro del túnel de TLS nunca se expone al punto de acceso inalámbrico: sólo el cliente y el servidor RADIUS pueden verlo.
  
3.  El servidor RADIUS comprueba las credenciales del cliente en relación con el directorio. Si el cliente se autentica correctamente, el servidor RADIUS recabará información con la que decidirá si autoriza al cliente a usar la WLAN. De esta forma, concede o deniega el acceso al cliente de acuerdo con la información del directorio (como la pertenencia a grupos) y también con las restricciones que se definen en la directiva de acceso correspondiente (por ejemplo, las horas del día en que es posible tener acceso a la WLAN). El servidor RADIUS transfiere la responsabilidad de decidir sobre el acceso al punto de acceso.
  
    Así, si el cliente obtiene acceso, el servidor RADIUS transmitirá la clave maestra del cliente al punto de acceso inalámbrico. Por su parte, el cliente y el punto de acceso comparten ahora material de claves comunes que pueden utilizar para cifrar y descifrar el tráfico de WLAN que fluye entre ellos.
  
    Cuando se utiliza una WEP dinámica para cifrar el tráfico, las claves maestras se utilizan directamente como clave de cifrado. Estas claves han de modificarse cada cierto tiempo para frustrar ataques de recuperación de claves WEP. El servidor RADIUS lleva esto a cabo obligando al cliente de forma periódica a volver a autenticarse y generar un conjunto de claves nuevo.
  
    En caso de que la comunicación se proteja mediante WPA, el material de clave maestra se usará para crear claves de cifrado de datos, que se modifican para cada paquete que se transmita. Con WPA no es necesario forzar la reautenticación para garantizar la seguridad de la clave.
  
4.  A continuación, el punto de acceso une la conexión de la WLAN del cliente a la LAN interna, lo que posibilita que el cliente se comunique con total libertad con los sistemas de la red interna. Así, ahora el tráfico que fluye entre el cliente y el punto de acceso está cifrado.
  
5.  En caso de que el cliente necesitara una dirección IP, podría solicitar el alquiler de un protocolo de configuración dinámica de host (DHCP) de un servidor de la LAN. Una vez se haya asignado la dirección IP, el cliente podrá empezar a comunicarse con normalidad con los restantes sistemas de la red.
  
#### Autenticación del equipo y del usuario en la WLAN
  
El proceso que se acaba de describir señala el modo en que un cliente (sea usuario o equipo) se conecta con éxito a la WLAN. Windows XP autentica tanto al usuario como al equipo de manera independiente. Cuando un equipo se inicia por primera vez, utiliza una cuenta de dominio y una contraseña para autenticarse en la WLAN. La autorización del equipo a la WLAN tiene lugar exactamente tal y como se ha especificado en la sección anterior. Aun cuando ningún usuario haya iniciado sesión, el equipo se podrá administrar si se conecta a la WLAN a través de sus propias credenciales. Por ejemplo, se podrá aplicar una configuración de directiva de grupo en el equipo, así como distribuir software y revisiones.
  
Cuando un usuario inicia sesión en el equipo, este proceso de autenticación y autorización se repite, pero, en este caso, con el nombre de usuario y la contraseña del usuario. La sesión de un usuario sustituye la sesión de WLAN del equipo, de modo que no hay dos sesiones activas al mismo tiempo. Además, esto evita que un usuario no autorizado utilice un equipo autorizado para obtener acceso a la WLAN.
  
**Nota:** Windows XP permite anular este comportamiento y especificar que sólo sirvan las credenciales del equipo o de un usuario. Estas configuraciones no son recomendables: la primera, porque permite que los usuarios se conecten a la WLAN sin autorización y la segunda, porque impide que el equipo pueda conectarse a la WLAN si no lo hace antes un usuario (lo que interferiría en varias de las funciones de administración de los equipos).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Perfil de la organización de destino
  
El diseño de esta solución está pensado para pequeñas empresas de entre 100 y 200 personas. Si bien la organización es ficticia, las características y requisitos son producto de una intensa investigación en el mundo real. Estos requisitos del mundo real han servido para modelar el estilo y el alcance de la guía, así como las preferencias de diseño.
  
Es importante comprender que esta solución no está limitada exclusivamente a organizaciones de este tamaño, dado que la sencillez del diseño y la escalabilidad de los componentes utilizados hacen de ella una solución de WLAN basada en PEAP adecuada para organizaciones mucho más pequeñas y mucho más grandes (con miles de usuarios). Si comprende las características de la organización de destino, sabrá con mayor seguridad las características del diseño y, en consecuencia, podrá adaptarlas a la organización.
  
El uso de esta solución en organizaciones de mayor envergadura se detalla en la sección "Escalabilidad para organizaciones más grandes" de este capítulo. En cuanto a aquellas organizaciones realmente pequeñas, todos los componentes pueden instalarse en un único servidor.
  
#### Diseño de la organización
  
La siguiente figura muestra el diseño físico y de tecnología de la información (TI) de la organización.
  
[![](images/Dd162271.PEAP_202(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_202_big(es-es,technet.10).gif)
  
**Figura 2.2. Diseño físico y de TI de la organización de destino**
  
Hay una gran oficina central donde se encuentran la mayoría de los sistemas de TI y gran parte de los usuarios. Todos los controladores de dominio de Active Directory se hallan aquí. La conexión a Internet en esta oficina se realiza a través de un servidor de seguridad. Existe un número de clientes WLAN y puntos de acceso inalámbrico conectados a la red interna.
  
También hay una o varias oficinas remotas con muy pocos servicios de TI locales aparte de la conexión de red con la oficina central. El número de clientes (todos inalámbricos, posiblemente) es pequeño en esta oficina, que con frecuencia recibe visitantes de la oficina central que disponen de sus propios clientes WLAN para que puedan volver a conectarse a sus aplicaciones y datos en la oficina central.
  
La conectividad de la red de área extensa (WAN) entre oficinas se suministra bien mediante líneas privadas (así, una T1 a 1,5 Mbps), bien mediante conexiones DSL y un vínculo entre enrutadores de una red privada virtual (VPN) a través de Internet. Normalmente, la conexión WAN es proclive a dar errores.
  
**Nota:** por lo general, cuando la conexión WAN entre oficinas se obtiene de una conexión VPN a través de Internet, cada oficina tiene un servidor de seguridad que la protege de las amenazas de Internet. En relación con la WLAN, el tema de la presencia de un servidor de seguridad no procede, de manera que se ha omitido en aras de una mayor claridad.
  
#### Entorno de TI
  
Active Directory, que en esta organización consiste en un solo bosque de dominios con al menos dos controladores de dominio, autentica usuarios en el dominio y proporciona servicios de directorio y autenticación a varias aplicaciones, como Microsoft Exchange Server y Outlook® para el correo electrónico. Los controladores de dominio han pasado recientemente de Windows 2000 Server a Windows Server 2003, versión Standard Edition. Para algunas aplicaciones heredadas, estos controladores de dominio ejecutan también otro tipo de servicios, como el Sistema de nombres de dominio (DNS), DHCP y el Servicio de nombres de Internet de Windows (WINS).
  
Los sistemas de TI son en su mayoría tecnologías Microsoft, con Windows XP en los equipos cliente y Windows Server 2003 en los sistemas servidor. Asimismo, existe un determinado número de servidores que ejecutan Windows 2000, algo que la compañía planea mejorar en tanto la prueba y la compatibilidad de las aplicaciones lo permitan. La organización empieza a invertir en sistemas móviles como Windows XP, Tablet Edition y Pocket PC 2003, en especial para el personal de ventas, de distribución y de almacén.
  
Entre las aplicaciones de servidor clave se incluyen Microsoft Exchange Server, SQL Server (que ejecuta varias aplicaciones de línea de negocios), Servicios de Internet Information Server (IIS) y Windows SharePoint™ Team Services.
  
Las aplicaciones se implementan en equipos cliente por medio de la directiva de grupo de Active Directory. En cuanto a las revisiones del sistema operativo, se implementan por medio de Microsoft Software Update Service (SUS) y el servicio Windows AutoUpdate.
  
El seguimiento del sistema se realiza directamente en los sistemas servidor mediante la revisión diaria de los registros de sucesos, los registros de rendimiento y los registros de aplicaciones. Las alertas importantes relativas al software y al hardware se envían al administrador de TI por medio de correos electrónicos y alertas en las consolas del sistema.
  
La organización cuenta con dos personas responsables de TI a tiempo completo que se encargan del planeamiento de TI, la entrega de servicios y la asistencia diaria. Tanto el administrador de TI como el ingeniero asistente de TI poseen las certificaciones MCSE más recientes y años de experiencia en este ámbito.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Criterios de diseño
  
La organización descrita en la sección anterior generalmente cumplirá con los siguientes tipos de criterios para una solución de WLAN. Estos criterios se han ampliado a fin de cubrir una amplia categoría de organizaciones. En el diseño presentado en el resto del capítulo se usan estos criterios de forma explícita.
  
**Tabla 2.1. Criterios de diseño de la solución de WLAN**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Factor de diseño</th>
<th style="border:1px solid black;" >Criterios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Requisitos de seguridad</td>
<td style="border:1px solid black;">-Una autenticación y autorización sólidas de los clientes inalámbricos.
-Un control de acceso sólido que permita el acceso de red a clientes autorizados y lo deniegue a clientes no autorizados.
-Un cifrado eficaz (128 bits) del tráfico de red inalámbrica.
-Una administración segura de las claves de cifrado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Escalabilidad: número mínimo/máximo de usuarios admitidos</td>
<td style="border:1px solid black;">De 25 a 5000 usuarios de WLAN (o más)
Consulte la tabla 2.2 para obtener información sobre las cargas de autenticación para distintos tamaños de WLAN.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Escalabilidad: número de sitios admitidos</td>
<td style="border:1px solid black;"><strong>Básico:</strong> un solo sitio de dimensiones considerables con controladores de dominio y servicios de TI locales; uno o más sitios pequeños sin controladores de dominio. El mínimo de usuarios que se precisa es 25.
<strong>Superior:</strong> un solo sitio central con varios controladores de dominio; oficinas grandes con un solo controlador de dominio y/o conectividad WAN resistente a la oficina central; varias oficinas pequeñas sin controlador de dominio, con una WAN probablemente poco resistente. El número máximo de usuarios permitido es 5000.
Para el uso en organizaciones grandes, consulte el apéndice A, &quot;Uso de PEAP en la empresa&quot;.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Requisitos de disponibilidad</td>
<td style="border:1px solid black;">Las oficinas de mayores dimensiones que utilicen varios puntos de acceso inalámbrico, IAS o controladores de dominio (inalámbricos) contarán con una WLAN resistente a un error de componente individual. Por el contrario, las WLAN de las oficinas pequeñas son vulnerables y con tendencia a producir errores, a menos que se instale una conectividad redundante.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Compatibilidad con plataformas</td>
<td style="border:1px solid black;"><strong>Plataformas del servidor:</strong> Windows Server 2003, versión Standard Edition o Enterprise Edition (para la instalación de IAS y de la entidad emisora de certificados). Standard Edition admite un máximo de 50 puntos de acceso inalámbrico (clientes RADIUS) por servidor.
<strong>Plataformas cliente:</strong> Windows XP Professional o Tablet Edition; Pocket PC 2003.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Extensibilidad (reutilización de los componentes de la solución para otras aplicaciones)</td>
<td style="border:1px solid black;">La misma infraestructura de autenticación puede admitir otras aplicaciones de acceso de red (VPN de acceso remoto, acceso a red por cable 802.1X y autenticación del servidor de seguridad).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Requisitos de la organización de TI</td>
<td style="border:1px solid black;">La instalación y la administración de la solución debe estar en manos de un experto de TI que posea la certificación MSCE más reciente o conocimiento equiparable, así como de 2 a 3 años de experiencia en el sector de TI.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Requisitos de capacidad de administración</td>
<td style="border:1px solid black;">La solución necesitará un mínimo de administración para mantener un funcionamiento sin problemas.
Las alertas se envían por correo electrónico o a través del registro de sucesos de Windows (o bien se modifican para desencadenar otros tipos de alerta).
El componente IAS se puede supervisar mediante la solución de supervisión de Windows (a través de registros de sucesos y contadores de rendimiento), mediante el registro de RADIUS y mediante el sistema de administración Protocolo simple de administración de redes (SNMP).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Cumplimiento de las normas</td>
<td style="border:1px solid black;">La solución admite las siguientes normas:
-Normas de red (a, b o g) IEEE 802.11.
-Autenticación IEEE 802.1X con PEAP y MS-CHAP v2, que puede usarse con otros métodos de EAP como el EAP-TLS basado en certificados y PEAP-EAP-TLS.
-WEP con clave dinámica y protección WPA para WLAN.
Capacidades y normas futuras (por ejemplo, 802.11i).
-Compatibilidad con RADIUS para RFC 2865 y 2866.</td>
</tr>
</tbody>
</table>
 

La siguiente tabla recoge una indicación de los requisitos de autenticación WLAN para diversos tamaños de organización. La columna "Nuevas autenticaciones por segundo" forma parte de la carga fija; en ella, se supone una media de cuatro autenticaciones nuevas por día y usuario, dado que los usuarios se desplazan por los puntos de acceso inalámbrico. La columna "Nuevas autenticaciones por segundo en hora máxima" señala el tipo de carga que se espera cuando todos los usuarios se autentican en un período de 30 minutos (por ejemplo, al inicio del día). La columna "Reautenticaciones por segundo" contempla el número de reautenticaciones regulares que obligan a una renovación de las claves WEP dinámicas.

**Tabla 2.2. Requisitos de autenticación de WLAN**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Número de usuarios de WLAN</th>
<th style="border:1px solid black;" >Nuevas autenticaciones por segundo</th>
<th style="border:1px solid black;" >Nuevas autenticaciones por segundo en hora máxima</th>
<th style="border:1px solid black;" >Reautenticaciones por segundo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">100</td>
<td style="border:1px solid black;">&gt; 0,1</td>
<td style="border:1px solid black;">0,1</td>
<td style="border:1px solid black;">0,1</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">1000</td>
<td style="border:1px solid black;">0,1</td>
<td style="border:1px solid black;">0,6</td>
<td style="border:1px solid black;">1,1</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">10000</td>
<td style="border:1px solid black;">1,4</td>
<td style="border:1px solid black;">5,6</td>
<td style="border:1px solid black;">11,1</td>
</tr>
</tbody>
</table>
  
Más adelante en este capítulo se hace referencia a estas cifras, en concreto, al tratar el tema de las dimensiones del servidor IAS.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Arquitectura de WLAN
  
Esta sección se centra en la arquitectura de la solución.
  
#### Diseño de la red
  
La siguiente figura ilustra el diseño de red básico para la oficina central.
  
[![](images/Dd162271.PEAP_203(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_203_big(es-es,technet.10).gif)
  
**Figura 2.3. Diseño de la red para la oficina central**
  
La figura muestra clientes inalámbricos, dos o más puntos de acceso inalámbrico, dos servidores IAS que se ejecutan en controladores de dominio de Active Directory, un servidor DHCP y otros servidores, clientes y dispositivos conectados a la red. A excepción de los clientes WLAN, todos los elementos se conectan a una sola LAN mediante uno o varios conmutadores de nivel 2. En este sitio se usa una única subred para toda la red interna. Existen conexiones enrutadas (que no aparecen en la figura) a través del servidor de seguridad a Internet y otras oficinas.
  
Es más probable que las organizaciones de mayores dimensiones tengan un entorno enrutado dentro de un único sitio. Esto no supone diferencia alguna para la infraestructura de autenticación, si bien puede influir en la manera en que los puntos de acceso inalámbrico se conectan con el resto de la red. Para que sea más sencillo que los usuarios se desplacen por los distintos puntos de acceso de un sitio, lo más normal es que se coloquen todos los puntos de acceso inalámbrico y todos los clientes WLAN en la misma subred de IP. Así, los usuarios podrán moverse por puntos de acceso inalámbrico manteniendo la misma dirección IP. Tratar este tema en mayor profundidad no se corresponde con los objetivos de esta guía. Encontrará más detalles al respecto en el capítulo sobre la implementación de una LAN inalámbrica del *Kit de distribución de Microsoft Windows Server 2003*.
  
En el diseño de la red, se debe garantizar los siguientes elementos:
  
-   Los puntos de acceso inalámbrico tienen conectividad con los servidores IAS tanto principales como secundarios. Así, en caso de que los puntos de acceso se encuentren en una VLAN/subred distinta de la de los servidores IAS, el tráfico deberá poder enrutarse entre tales subredes.
  
-   Los clientes WLAN deben tener conectividad a los servidores DHCP. Si los servidores no se hallaran en la misma subred, será necesario tener agentes de retransmisión DHCP/BOOTP para reenviar solicitudes DHCP del cliente a un DHCP que posea un ámbito definido para esa subred. Sobra decir que los clientes necesitarán conectividad a los servicios de red normales, como los controladores de dominio, servidores de archivos, etc.
  
#### Selección del hardware de la red inalámbrica
  
Debe garantizar que los puntos de acceso inalámbrico y los adaptadores de red inalámbricos sean compatibles con los siguientes elementos:
  
-   Cifrado de WEP de 128 bits (si se usa una WEP dinámica), cifrado de TKIP (RC4) o cifrado de AES (se usa WPA).
  
-   Autenticación 802.1X.
  
-   Actualización de la clave dinámica (sólo cifrado de WEP).
  
-   Compatibilidad con WPA (aun cuando se use una WEP dinámica, debería tener un compromiso firme por parte del proveedor para que suministre actualizaciones de firmware con las que poder admitir WPA).
  
Debe tener suficientes puntos de acceso inalámbrico para proporcionar cobertura para clientes WLAN a través de ubicaciones físicas con las que ha de ser compatible. Asimismo, debe planear la colocación de esos puntos de acceso inalámbrico para que, en caso de que se produzca un error en uno de ellos, exista una cobertura de copia de seguridad adecuada en todas las ubicaciones. El tema de la colocación de los puntos de acceso inalámbrico se trata en mayor profundidad en el capítulo sobre la implementación de una LAN inalámbrica del *Kit de distribución de Microsoft Windows Server 2003*, que se incluye igualmente en la sección "Referencias" al final de este capítulo. También es aconsejable que lea el artículo "Recommendations for IEEE 802.11 Access Points", al que se hace referencia al final de este capítulo.
  
#### Colocación del servidor IAS
  
El objetivo de la colocación del servidor IAS reside en obtener un servicio de WLAN resistente con costes de implementación y administración moderados. Un servicio de WLAN que ofrece resistencia a un error de componente individual presenta las siguientes características:
  
-   Todas las áreas físicas que precisen cobertura de WLAN deben tener un mínimo de dos puntos de acceso inalámbrico dentro de su alcance.
  
-   Cada punto de acceso inalámbrico debe poder comunicarse con un servidor IAS de copia de seguridad en caso de que el principal no funcione o que la conexión de red a este servidor no pueda establecerse.
  
-   Los servicios de los que tanto IAS como los clientes WLAN dependen (por ejemplo, Active Directory, DHCP y DNS) deben ofrecer la misma resistencia.
  
La segunda característica es la más importante a la hora de planear la colocación del servidor IAS. En esta solución, IAS se encuentra en controladores de dominio ya existentes, con lo que se obtiene la mejor configuración de rendimiento con un coste de implementación y administración relativamente bajo. Como recomendación general para cualquier organización (sea del tamaño que sea), IAS se debe implementar en todos los sitios que tengan un controlador de dominio (si bien no tiene por qué instalarse en cada uno de estos controladores).
  
La siguiente figura recoge la colocación de servidores IAS en la organización. En este caso, IAS se implementa en dos controladores de dominio en la oficina central. La entidad emisora de certificados de la red (consulte la sección "Obtención de certificados para servidores IAS" más adelante en este capítulo) también se instala en uno de estos controladores de dominio. Todos los puntos de acceso inalámbrico en la oficina central se configuran con el fin de utilizar estos servidores IAS.
  
[![](images/Dd162271.PEAP_204(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_204_big(es-es,technet.10).gif)
  
**Figura 2.4. Infraestructura de la oficina central y de la sucursal**
  
La organización tiene una pequeña sucursal sin controlador de dominio local. Los puntos de acceso inalámbrico en este sitio emplean los dos servidores IAS de la oficina central para todas las solicitudes de autenticación; es decir, los usuarios no podrán autenticarse en la WLAN si se produce un error en la conexión WAN de la oficina central. Esto constituye un riesgo que muchas organizaciones no pueden permitirse.
  
Para resolver esto, debería instalar una conectividad WAN redundante, o bien instalar un IAS y un controlador de dominio locales. Si bien puede considerarse como un coste inaceptable para este tipo de oficina, un error en WAN podría provocar igualmente que muchos otros servicios de red no funcionaran adecuadamente (por ejemplo, los servidores de archivos locales) sin acceso a un controlador de dominio. En consecuencia, si soluciona esto, la confiabilidad tanto de estos servicios como de la WLAN local mejorará considerablemente. La implementación de controladores de dominio en sucursales se detalla en la sección "Escalabilidad para organizaciones más grandes" más adelante en este capítulo.
  
En relación con oficinas pequeñas donde la conectividad WAN es muy poco confiable y donde la implementación de un controlador de dominio no es viable, puede optar por implementar una WLAN independiente. Para obtener más información, lea la sección "Entornos SOHO" más adelante en este capítulo.
  
#### Asignación de puntos de acceso a servidores RADIUS
  
Debe asignar todos los puntos de acceso inalámbrico a servidores IAS. Cada punto de acceso inalámbrico necesita un servidor RADIUS principal y uno secundario, ya que, así, podrá usar el servidor RADIUS secundario en caso de que no pueda ponerse en contacto con el principal o éste no funcione. Esta disposición se muestra en la siguiente figura.
  
![](images/Dd162271.PEAP_205(es-es,TechNet.10).gif)
  
**Figura 2.5. Equilibrio del punto de acceso entre los servidores IAS principal y secundario**
  
La figura muestra el modo en que cada uno de los puntos de acceso inalámbrico se configura con un servidor RADIUS principal y uno secundario distintos. Esto permite el equilibrio de carga entre ambos servidores. Los puntos de acceso inalámbrico en sitios que carecen de un servidor IAS local seguirán la misma pauta, pero usando los servidores IAS de la oficina central como servidores RADIUS principal y secundario.
  
En el caso de los puntos de acceso inalámbrico en sitios que sólo tienen un servidor IAS local, éste siempre ha de ser el principal, mientras que el de la oficina central (u otra ubicación pertinente donde exista conectividad a un servidor IAS confiable) será el secundario. Esta configuración se ilustra en la figura siguiente.
  
[![](images/Dd162271.PEAP_206(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_206_big(es-es,technet.10).gif)
  
**Figura 2.6. Configuración de los puntos de acceso para usar servidores IAS locales y remotos**
  
Si posee una gran cantidad de puntos de acceso, debería documentar minuciosamente la asignación de éstos a servidores IAS. De este modo, podrá usar este registro para garantizar que cada punto de acceso tiene asignado un servidor principal y otro secundario y, asimismo, que la carga desde estos puntos presenta un equilibrio uniforme entre los servidores disponibles.
  
**Nota:** si el servidor IAS no está disponible, todos los puntos de acceso inalámbrico realizarán una conmutación por error hacia el servidor IAS secundario. No obstante, la mayoría de los puntos de acceso no volverán a usar el principal automáticamente una vez éste vuelva a estar disponible (sólo lo harán en caso de que se produzca un error posterior en el secundario). Esto no supone un problema de importancia cuando los dos servidores IAS se hallan en la misma ubicación, sino que, simplemente, la carga entre los servidores no será uniforme. Ahora bien, si el servidor IAS secundario es remoto, es posible que un error en el servidor principal provoque que todos los puntos de acceso se autentiquen en el servidor secundario a través de un vínculo WAN que no sea óptimo.
  
En caso de que los puntos de acceso no vuelvan de manera automática al servidor principal designado, es probable que necesite restablecer manualmente los puntos de acceso para que, así, comiencen a usar el servidor IAS local una vez se haya recuperado tras un error. Las condiciones de red transitorias también pueden ser motivo de conmutación por error de los puntos de acceso hacia los servidores RADIUS secundarios, de manera que puede que sea necesario comprobar de forma ocasional los sucesos de solicitud de autenticación en los registros de aplicación de servidores IAS con el fin de detectar cualquier punto de acceso que esté utilizando el IAS inapropiado.
  
#### Co-ubicación de IAS con controladores de dominio
  
En esta solución, IAS se instala en los controladores de dominio existentes. De esta forma, los costes de implementación se mantienen bajos y se consigue una mejora del rendimiento a través del uso de IAS en un servidor miembro independiente. Esta mejora se produce porque el IAS puede comunicarse con Active Directory en el mismo equipo sin que tenga lugar retraso alguno en la red.
  
No olvide que hay una serie de salvedades relativas a la instalación de IAS en controladores de dominio. Bien es cierto que no tienen por qué condicionar a muchas organizaciones, pero puede que sea interesante tenerlas en consideración antes de proceder:
  
-   No podrá tener una configuración única para todos los controladores de dominio, a menos que opte por instalar IAS en todos ellos.
  
-   No podrá imponer la separación entre la administración de IAS y la administración del dominio. La instalación de IAS en los controladores de dominio significa que los administradores de IAS deben ser miembros también del grupo de administradores de dominio incrustado.
  
-   Una gran carga de las funciones de los controladores de dominio podría afectar de forma negativa al rendimiento de IAS y viceversa. Así, puede que quiera depositarlas en servidores independientes para ejercer un mayor control sobre el rendimiento individual y el funcionamiento de estos servicios.
  
#### Requisitos del software y del hardware de IAS
  
En una organización de destino de entre 100 y 200 usuarios, es bastante improbable que la carga de IAS en los servidores sea motivo de problema en tanto se use la especificación de hardware recomendada para Windows Server 2003. No obstante, en el caso de organizaciones de mayor tamaño, este aspecto ha de tenerse en cuenta si IAS se ejecuta en los controladores de dominio existentes.
  
La carga en IAS podrá verse afectada por los siguientes aspectos:
  
-   Número de usuarios y dispositivos que requieren autenticación de RADIUS.
  
-   Elección de las opciones de autenticación tales como el tipo de EAP y la frecuencia de reautenticación.
  
-   Si el registro de RADIUS está habilitado.
  
Puede hacer uso de las cifras que recoge la tabla 2.2 de la sección anterior, "Criterios de diseño", para calcular el número de autenticaciones por segundo que pueden preverse de una población determinada. Debería tenerse en cuenta la carga de estado fija cuando los usuarios se autentican de manera habitual y, al mismo tiempo, la carga del "peor caso" en horas punta. Si se extrapolan las cifras de esta tabla, 200 usuarios generan una carga de estado fija inferior a una autenticación completa cada 50 segundos, así como una reautenticación rápida cada 10 segundos. Se trata de cifras tan insignificantes, que la única relevante es el tiempo que se tarda en autenticar a todos los usuarios tras una interrupción de la actividad, cuando todos los usuarios necesitan volver a conectarse a la WLAN de inmediato. Este momento constituye una hora punta bastante más acusada que el primer inicio de sesión del día, que tiende a prolongarse unos 30 minutos o más.
  
Las opciones de autenticación tienen un gran efecto en la carga del servidor IAS. Los protocolos como PEAP realizan una operación de clave pública con gran actividad de la CPU durante el primer inicio de sesión, si bien emplean información de sesiones en caché para reautenticaciones posteriores (lo que se conoce como "reconexión rápida"). Si utiliza una WEP dinámica, los clientes se reautenticarán cada 15-60 minutos para generar nuevas claves de cifrado. Sin embargo, en el caso de WPA, deberá forzar la reautenticación con mucha menos frecuencia, normalmente cada 8 horas.
  
La siguiente tabla refleja el número aproximado de autenticaciones que se producen por segundo en un IAS en un servidor Intel Pentium 4 a 2 GHz que ejecuta Windows Server 2003 con Active Directory en un servidor independiente.
  
**Nota:** la información contenida en la tabla, producto de una serie de pruebas que Microsoft Solutions for Security ha realizado, se ofrece sin garantía alguna y sólo se debe utilizar como orientación a la hora de planear la capacidad y no para realizar comparaciones de rendimiento.
  
**Tabla 2.3. Autenticaciones por segundo**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Tipo de autenticación</th>
<th style="border:1px solid black;" >Nuevas autenticaciones</th>
<th style="border:1px solid black;" >Autenticaciones de reconexión rápida</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Autenticaciones PEAP por segundo</td>
<td style="border:1px solid black;">36</td>
<td style="border:1px solid black;">166</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Tiempo de autenticación de 200 usuarios</td>
<td style="border:1px solid black;">6 segundos</td>
<td style="border:1px solid black;">2 segundos</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Tiempo de autenticación de 1000 usuarios</td>
<td style="border:1px solid black;">30 segundos</td>
<td style="border:1px solid black;">7 segundos</td>
</tr>
</tbody>
</table>
  
Estas cifras se han calculado con el registro de RADIUS habilitado y con Active Directory ejecutándose en un servidor independiente. Ambos factores reducen el rendimiento de IAS, de manera que esta estimación podría considerarse pesimista.
  
Tal y como ponen de manifiesto estas cifras, este tipo de servidor permitirá que 200 usuarios de la WLAN se autentiquen en la red en 6 segundos y 1000 usuarios, en 30.
  
#### Uso de Windows Server Standard o Enterprise Edition
  
En esta solución se usa Windows Server 2003, versión Standard Edition, para todos los servidores IAS; así, los costes de las licencias de los servidores se mantienen bajos y, además, podrá realizar implementaciones en servidores ya existentes, sean éstos Standard o Enterprise Edition.
  
IAS en la versión Standard Edition de Windows Server 2003 está limitada para que cada servidor admita sólo 50 clientes RADIUS y dos grupos de enrutamiento de servidores RADIUS.
  
**Nota:** un cliente RADIUS no es lo mismo que un cliente WLAN. Un cliente RADIUS hace referencia a puntos de acceso inalámbrico y también a otros servidores de acceso a la red (como servidores VPN y servidores de seguridad) que emplean los servicios de autenticación de RADIUS.
  
Un máximo de 50 puntos de acceso por servidor es más que suficiente para las organizaciones de destino de entre 1 y 200 usuarios. En el caso de organizaciones de dimensiones mayores, este límite podría ser especialmente relevante para las oficinas más grandes o cuando muchas oficinas satélite se conectan a uno o dos servidores IAS de concentrador.
  
En el supuesto de que haya 15 usuarios por punto de acceso inalámbrico, quiere decir que un solo servidor IAS en Windows Server 2003, versión Standard Edition, podría admitir hasta aproximadamente 750 usuarios. En esta estimación se tiene presente el número total de puntos de acceso que van a usar un servidor como un servidor RADIUS principal o secundario; en consecuencia, dos servidores admiten 50 puntos de acceso y no 100. En caso de que alguno de los servidores IAS deban admitir más de 50 puntos de acceso, necesitará la versión Enterprise Edition de Windows Server 2003. Obviamente, se pueden combinar ambas ediciones o hacerlas coincidir utilizando Windows Server 2003, Enterprise Edition para oficinas más grandes y oficinas con concentrador y Windows Server 2003, Standard Edition para oficinas más pequeñas.
  
#### Configuración de IAS
  
La configuración de IAS puede dividirse en cuatro categorías principales:
  
-   Configuración del servidor IAS
  
-   Configuración del registro de RADIUS
  
-   Directivas de acceso remoto
  
-   Directivas de solicitud de conexión
  
Estas categorías se describen detalladamente en las siguientes subsecciones. Estas configuraciones se pueden realizar en un solo servidor IAS y copiarlas en el resto, dado que son comunes a todos los servidores IAS que se usan en esta solución. Esta técnica se aplica en el capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas", con el fin de garantizar que la configuración de IAS sea coherente en todos los servidores de la organización.
  
Asimismo, cada servidor IAS tendrá uno o varios puntos de acceso inalámbrico configurados como clientes RADIUS. El tema de los clientes RADIUS se trata en la sección anterior "Asignación de puntos de acceso a servidores RADIUS". El grupo de clientes RADIUS es generalmente distinto en cada servidor y, por lo tanto, no se replican entre servidores de la misma forma que el resto de configuraciones.
  
#### Configuración del servidor IAS
  
En esta categoría se incluyen los siguientes elementos:
  
-   Registro de las solicitudes de autenticación en el registro de sucesos de Windows. En esta solución se habilita el registro tanto de los sucesos correctos como de los erróneos.
  
    **Nota:** el registro de solicitudes se detalla en la sección "Registro de RADIUS" más adelante en este capítulo.
  
-   Puertos de Protocolo de datagramas de usuarios (UDP) que el servidor IAS escucha para las solicitudes de autenticación y de responsabilidad de RADIUS. En esta solución se utilizan los puertos de RADIUS 1812 y 1813 para la autenticación y la contabilidad respectivamente.
  
#### Directivas de RADIUS
  
Las directivas de servidor IAS controlan la autenticación y la autorización de las cuentas en la red. Existen dos tipos de directivas:
  
-   Directiva de acceso remoto.
  
-   Directiva de solicitud de conexión.
  
La directiva de acceso remoto controla si se autoriza una conexión en la red y el modo en que se hace. Este tipo de directiva contiene un grupo de condiciones de filtro que determinan si la directiva es apropiada para una solicitud de conexión concreta. Algunos ejemplos de condiciones de filtro son: especificación del grupo de seguridad de Windows al que un cliente debe pertenecer; especificación del tipo de conexión (inalámbrica, VPN, etc.) del cliente que realiza la solicitud, y especificación del momento del día en que el cliente intenta conectarse. Cada directiva de acceso remoto posee una acción de directiva, que se establece en *permitir* o *denegar* una solicitud de conexión. Las solicitudes de conexión que coincidan con el filtro de condición de la directiva de acceso remoto obtendrán permiso de acceso o no en función de la configuración de esta acción de directiva.
  
Asimismo, una directiva de acceso remoto contiene una serie de parámetros que se aplican a una conexión permitida, conocidos como perfil de directiva de acceso remoto. Estos parámetros incluyen los métodos de autenticación que se consideran aceptables para esta conexión, el modo en que una dirección IP se asigna al cliente y la cantidad de tiempo durante la que el cliente puede permanecer conectado antes de que la reautenticación sea necesaria. Pueden existir muchas directivas de acceso remoto en un IAS. Así, cada solicitud de conexión se evalúa en relación con éstas (por orden de prioridad), hasta que una directiva coincidente permita o deniegue la solicitud.
  
La directiva de acceso remoto en esta solución se configura tal y como se muestra en la tabla siguiente:
  
**Tabla 2.4. Configuración de directivas de acceso remoto**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Elemento de configuración</th>
<th style="border:1px solid black;" >Configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Nombre de directiva</td>
<td style="border:1px solid black;">Permitir acceso a LAN inalámbrica</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Tipo de directiva</td>
<td style="border:1px solid black;">Permitir</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Condiciones de directiva de acceso remoto</strong></td>
<td style="border:1px solid black;"><br />
</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Coincidencias de tipo de puerto NAS</td>
<td style="border:1px solid black;">IEEE 802.11 inalámbrico
Otros dispositivos inalámbricos</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Coincidencias del grupo de Windows</td>
<td style="border:1px solid black;">Acceso a LAN inalámbrica</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Perfil de directiva de acceso remoto</strong></td>
<td style="border:1px solid black;"><br />
</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Restricciones de marcado: tiempo de espera del cliente</td>
<td style="border:1px solid black;">60 minutos (WEP dinámica)
8 horas (WPA)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Asignación de dirección IP</td>
<td style="border:1px solid black;">La configuración del servidor determina la asignación de la IP</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Filtrado IP</td>
<td style="border:1px solid black;">Ninguno</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Autenticación</td>
<td style="border:1px solid black;">Todo deshabilitado aparte de EAP</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Autenticación: tipo de EAP empleado</td>
<td style="border:1px solid black;">EAP protegido (PEAP)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Autenticación: tipo de PEAP empleado</td>
<td style="border:1px solid black;">EAP MS-CHAP v2</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Autenticación: reconexión rápida</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Atributos RADIUS</td>
<td style="border:1px solid black;">Ignorar propiedades de acceso telefónico del usuario = &quot;True&quot;
Acción terminación = &quot;RADIUS-Request&quot;</td>
</tr>
</tbody>
</table>
 

El filtro de condiciones coincide con todos los clientes inalámbricos y con todos los miembros del grupo de dominio de acceso a LAN inalámbrica. La tabla no contempla aquellos parámetros que no sean relevantes para el acceso a WLAN, como puedan ser Multilink o el cifrado punto a punto de Microsoft (MPPE). Para obtener más detalles sobre el uso de los grupos de seguridad con la directiva de acceso remoto, consulte la sección "Modelo de administración de usuario y equipo de WLAN" más adelante en este capítulo.

La configuración Restricciones de marcado: tiempo de espera del cliente puede incidir en la seguridad y en la confiabilidad de la solución. Los motivos por los que han de usarse valores distintos a los recogidos en la tabla se exponen en la sección "Opciones de seguridad para la WEP dinámica" más adelante en este capítulo.

El atributo RADIUS "Ignorar-propiedades-de-acceso-telefónico-del-usuario" se utiliza para omitir el control de los permisos de acceso a la red por usuario. Consulte la sección "Modelo de administración de usuario y equipo de WLAN" para obtener una explicación del control del acceso por usuario y por grupo.

Una directiva de solicitud de conexión controla si la solicitud se procesa en un servidor RADIUS concreto o si se envía a otro distinto (conocido como proxy RADIUS). Normalmente, un proxy RADIUS se utiliza cuando un servidor RADIUS no posee la información necesaria para procesar la solicitud por sí mismo y, por lo tanto, debe reenviarlo a un servidor RADIUS autoritativo (por ejemplo, a un servidor en otro bosque de Active Directory). Los servidores proxy RADIUS no se utilizan en esta solución y no competen a esta guía.

Para obtener más información sobre las directivas de solicitud de acceso remoto y de solicitud de conexión, así como sobre el uso de los servidores proxy RADIUS, consulte la sección "Referencias" al final de este capítulo.

#### Registro de RADIUS

Puede configurar los servidores IAS para registrar dos tipos de información opcional:

-   Sucesos de autenticación aceptados y rechazados.

-   Información de autenticación y cuentas de RADIUS.

Los sucesos de autenticación aceptados y rechazados generados a partir de dispositivos y usuarios de WLAN se pueden registrar en el registro de sucesos del sistema Windows Server 2003 del servidor IAS. La información que el registro de sucesos de autenticación contiene es muy útil para la solución de problemas de autenticación, aunque también se puede utilizar con fines de alerta y auditoría de seguridad.

Puede considerar deshabilitar los sucesos aceptados una vez que el sistema se haya estabilizado, si bien, en un principio, el registro de sucesos aceptados y rechazados debe dejarse habilitado. El motivo reside en que, pese a que los sucesos de acceso a WLAN aceptados inunden el registro de sucesos del sistema, puede que sean necesarios para fines de auditoría.

Si utiliza una herramienta de supervisión y alerta como Microsoft Operations Manager (MOM), debería considerar la idea de agregar una regla para avisar de los sucesos de error en la autenticación de IAS en el registro de sucesos del sistema. Otra opción consiste en usar una herramienta de consulta del registro de sucesos como eventquery.vbs para comprobar el registro de sucesos en busca de errores de autenticación (consulte la entrada "Eventquery.vbs" en la ayuda en línea). Por lo general, los sucesos individuales son de poca importancia, pero una serie de dichos sucesos podría indicar que se ha intentado irrumpir en el sistema.

IAS también ofrece la posibilidad de registrar información de la sesión de autenticación y del acceso a la red en forma de registros de solicitudes de RADIUS. Por lo general, el registro de RADIUS se emplea cuando es preciso cobrar por el uso de la red (por ejemplo, como proveedor de un servicio Internet (ISP), ha de cobrar en función del tiempo de conexión) o bien cuando es necesario contar con información de auditoría de seguridad especializada (aunque en la mayoría de los casos esto ya lo cubren los sucesos de autenticación registrados en el registro de sucesos).

Para obtener más información sobre el registro de RADIUS, consulte la sección "Referencias" al final del capítulo.

#### Seguridad IAS

Las precauciones de seguridad para IAS deben ser las mismas que se usan para un controlador de dominio. Un control seguro de la red depende de la seguridad de la infraestructura de IAS. Para mejorar la seguridad de IAS, puede implementar una serie de medidas sencillas:

-   Utilice contraseñas seguras para los clientes RADIUS (puntos de acceso inalámbrico). La solución incluye secuencias de comandos para generar contraseñas verdaderamente aleatorias que dificulten los ataques de diccionario.

-   Habilite el autenticador de mensajes de RADIUS en todos los clientes RADIUS a fin de evitar la imitación de direcciones IP de los puntos de acceso inalámbrico. En esta solución, esta opción está habilitada.

-   Asegúrese de que la configuración de seguridad del servidor es la adecuada. Esto se trata en el capítulo 3, "Preparación del entorno".

-   Asegúrese de que se han aplicado las revisiones de seguridad más recientes en el servidor y, asimismo, que se obtienen revisiones actualizadas de forma periódica. Esto también se incluye en el capítulo 3, "Preparación del entorno".

-   Asegúrese de que usa una configuración de cuenta de dominio segura. En concreto, debería asegurarse de que se utilizan contraseñas seguras y de que se cambian con regularidad. Igualmente, no olvide habilitar el bloqueo de cuenta de dominio para bloquear los ataques de averiguación de contraseña. No obstante, se recomienda habilitar únicamente el bloqueo de cuentas en caso de que tenga los recursos de soporte con los que desbloquear las cuentas de los usuarios de manera puntual.

-   Considere utilizar IPSec para proteger el tráfico de RADIUS y reforzar la autenticación mutua entre los puntos de acceso inalámbrico y los servidores IAS. No obstante, no todos los puntos de acceso inalámbrico son compatibles con IPSec.

Para obtener más información sobre las medidas de seguridad de IAS, consulte la sección "Referencias" al final del capítulo.

#### Modelo de administración de usuario y equipo de WLAN

El acceso a la WLAN en esta solución se controla por medio de grupos de seguridad de dominio. Bien es cierto que se puede hacer uso de las propiedades de acceso telefónico de los objetos de usuario de dominio para admitir o denegar el acceso a elementos individuales, pero esto supondría una tarea de administración muy pesada para muchos de los usuarios.

La solución emplea un esquema realmente básico para conceder el acceso a WLAN a todos los usuarios y equipos del dominio. Para muchas organizaciones, el control del acceso a través de la pertenencia al dominio es ya lo suficientemente seguro y reduce la carga de administración adicional asociada a la WLAN. En el caso de algunas organizaciones que precisan un control mayor, no obstante, pueden emplearse grupos de seguridad para definir quién tiene permiso para tener acceso a la WLAN.

Tal y como se describe en la sección "Directivas de RADIUS", la directiva de acceso remoto en un IAS utiliza una condición de filtro que concede acceso a WLAN a todos los miembros del grupo de acceso a la LAN inalámbrica. En la tabla siguiente se plasma la pertenencia del grupo de acceso a la LAN inalámbrica.

**Tabla 2.5. Grupos de acceso inalámbrico para permitir a todos los usuarios y equipos**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupo universal de nivel superior (acceso concedido en la directiva de acceso remoto)</th>
<th style="border:1px solid black;" >Miembros de primer nivel
(grupos globales de dominio)</th>
<th style="border:1px solid black;" >Miembros de segundo nivel
(grupos globales de dominio)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Acceso a LAN inalámbrica</td>
<td style="border:1px solid black;">Usuarios de LAN inalámbrica</td>
<td style="border:1px solid black;">Usuarios de dominio</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Acceso a LAN inalámbrica</td>
<td style="border:1px solid black;">Equipos de LAN inalámbrica</td>
<td style="border:1px solid black;">Equipos de dominio</td>
</tr>
</tbody>
</table>
  
El grupo de la primera columna, Acceso a LAN inalámbrica, tiene dos miembros enumerados en la segunda columna, esto es, Usuarios de LAN inalámbrica y Equipos de LAN inalámbrica. Estos grupos "de primer nivel" contienen miembros (que aparecen en la tercera columna, "Miembros de segundo nivel"), esto es, los grupos de usuarios de dominio y de equipos de dominio respectivamente. Esta disposición de grupos anidados posibilita que todos los usuarios y equipos del dominio se conecten a WLAN.
  
Si resulta excesivamente permisivo para la organización que todos los usuarios y equipos tengan acceso a WLAN, puede eliminar a unos u otros de estos grupos. De ser así, deberá agregar las cuentas o grupos de usuario y de equipo concretas a los grupos de LAN inalámbrica. En la tabla siguiente se refleja el modo de usar la estructura de grupos de acceso a la LAN inalámbrica de la forma descrita.
  
**Tabla 2.6. Grupos de acceso inalámbrico para permitir a usuarios y equipos seleccionados**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupo universal de nivel superior (acceso concedido en la directiva de acceso remoto)</th>
<th style="border:1px solid black;" >Miembros de primer nivel (grupos globales de dominio)</th>
<th style="border:1px solid black;" >Miembros de segundo nivel
(grupos globales de dominio)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Acceso a LAN inalámbrica</td>
<td style="border:1px solid black;">Usuarios de LAN inalámbrica</td>
<td style="border:1px solid black;">Usuario1<br />
Usuario2
Usuario3</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Acceso a LAN inalámbrica</td>
<td style="border:1px solid black;">Equipos de LAN inalámbrica</td>
<td style="border:1px solid black;">Equipo1<br />
Equipo2<br />
Equipo3</td>
</tr>
</tbody>
</table>
 

Para obtener más información sobre el uso de estos grupos de seguridad en un bosque con varios dominios, consulte la sección "Escalabilidad para organizaciones más grandes" más adelante en este capítulo.

#### Obtención de certificados para servidores IAS

Los servidores IAS requieren tener certificados para autenticar a los clientes WLAN. Los certificados de servidor son necesarios para crear el túnel cifrado de TLS entre servidores IAS y clientes. TLS sirve para proteger el intercambio de autenticaciones entre el servidor y los clientes.

**Nota:** TLS constituye un estándar de RFC basado en la versión similar de capa de sockets seguros 3.0 (SSL 3.0). Ambos se emplean habitualmente para proteger el tráfico Web como parte del Protocolo de transferencia de hipertexto seguro (HTTPS).

#### Entidad emisora de certificados incrustada frente a entidad emisora de certificados comercial

Para obtener estos certificados, puede optar por instalar una entidad emisora por sí mismo o bien adquirir los certificados de un proveedor de certificados comercial. Ambas posibilidades son válidas y decantarse por una u otra no supone una diferencia técnica real para la solución de WLAN.

La tabla que sigue a continuación muestra las ventajas y los inconvenientes principales de usar una entidad emisora de certificados interna en lugar de comprar certificados a un proveedor comercial.

**Tabla 2.7. Ventajas e inconvenientes de usar una entidad emisora de certificados propia frente a certificados comerciales**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Entidad emisora interna</th>
<th style="border:1px solid black;" >Entidad emisora comercial</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Sin coste por certificado</td>
<td style="border:1px solid black;">Coste por certificado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">El software de la entidad emisora de certificados debe instalarse y administrarse</td>
<td style="border:1px solid black;">No hay software de servidor</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Inscripción y renovación automáticas</td>
<td style="border:1px solid black;">Proceso de inscripción más complejo, instalación manual de los certificados</td>
</tr>
</tbody>
</table>
  
El equilibrio del argumento se basa en la complejidad y el coste de la administración de la entidad emisora de certificados propia. Así, si el coste de la configuración de una entidad emisora de certificados local es moderado y la administración sencilla, normalmente resulta más atrayente que la opción de adquirir certificados externos.
  
Esta solución emplea una entidad emisora interna y sencilla para proporcionar los certificados. Los términos "entidad emisora de certificados incrustada" y "entidad emisora de certificados de red" se han usado en la presente guía para señalar que se trata de una entidad emisora con un propósito especial; en esencia, esta entidad no es visible para usuarios y administradores, y expide certificados de una sola clase. La funcionalidad limitada de la entidad emisora de certificados en esta solución quiere decir que se puede instalar y usar sin administración o intervención alguna del usuario. Por ejemplo, en esta solución, la entidad emisora de certificados puede expedir un certificado que tenga una duración de 25 años, de manera que no tendrá que renovarlo durante la vigencia de la solución. La inscripción y renovación automáticas de los certificados del servidor IAS indican que no hay que realizar una distribución manual de los certificados.
  
Compare esto con el uso de certificados externos. Recuerde que debe renovar los certificados de todos los servidores IAS cada año o cada dos años, lo que significa crear manualmente la solicitud de certificado en todos los servidores IAS, enviar la solicitud a la entidad emisora de certificados comercial y, finalmente, obtener el certificado expedido e instalarlo manualmente. Si esto no se lleva a cabo, impedirá que los usuarios se conecten a la WLAN. Para muchas organizaciones, esto supone una carga administrativa mucho más pesada que la entidad emisora de certificados interna básica utilizada en esta solución.
  
#### Limitaciones de la entidad emisora de certificados de la solución
  
Esta solución usa una configuración de entidad emisora de certificados especial para expedir certificados para los servidores IAS. Se ha diseñado con el único propósito de cubrir esta necesidad concreta, de modo que no se trata de una autoridad de certificaciones con fines generales.
  
Los certificados digitales se emplean en muchas aplicaciones, entre otras, el correo electrónico seguro y la exploración Web, la seguridad IP (IPSec), las redes privadas virtuales (VPN) o el sistema de cifrado de archivos (EFS). Cada una de estas aplicaciones posee sus propios requisitos de seguridad. Su organización tendrá una serie de requisitos de seguridad propios y exclusivos de acuerdo con estas aplicaciones. Por estos motivos, Microsoft recomienda enormemente no usar la entidad emisora de certificados de la solución con cualquier otro propósito.
  
Si tiene intención de usar esas u otras aplicaciones de certificado, diseñe una infraestructura de certificados de acuerdo a los requisitos correspondientes. Algunos de los aspectos que debe tener en cuenta son:
  
-   La entidad emisora de certificados de la solución es una entidad emisora raíz con firma personal, de manera que no se puede revocar (los certificados expedidos se revocan en caso de compromiso de la entidad emisora).
  
-   Es posible que la legislación industrial o específica de cada país obligue al uso de una jerarquía de varios niveles de entidades emisoras para algunos o todos los tipos de certificado.
  
-   Microsoft no recomienda la instalación de una entidad emisora de certificados en un controlador de dominio en el caso de certificados de alta seguridad.
  
Para obtener más información sobre el planeamiento detallado que se necesita para diseñar una arquitectura de infraestructura de claves públicas más general, consulte el capítulo 4, "Diseño de la infraestructura de claves públicas", de la solución complementaria, *Solución de Seguridad de LAN inalámbricas — Servicios de Certificate Server de Microsoft Windows Server 2003*.
  
También se ha de tener en cuenta que existe un número de limitaciones cuando la entidad emisora de certificados se instala en la versión Standard Edition de Windows Server 2003, que, aunque adecuada para la solución, es compatible con una serie limitada de funcionalidades en comparación con la versión Enterprise Edition de Windows Server 2003. Entre las características más destacadas de las que no se puede disponer en la versión Enterprise Edition de Windows Server 2003 se incluyen las siguientes:
  
-   **Inscripción automática de certificados para equipos y usuarios:** el servicio de solicitud de certificados automática (que se usa en Windows 2000 Server y Windows Server 2003, Standard Edition) no permite la inscripción automática de certificados para el usuario, ya que sólo es compatible con la inscripción automática de certificados de equipo.
  
-   **Plantillas de certificado de la versión 2:** muchos de los tipos de certificado utilizados en Windows Server 2003 y en Windows XP emplean las características avanzadas de las plantillas de la versión 2. Sin embargo, una entidad emisora basada en la versión Standard Edition de Windows Server 2003 no puede expedir certificados en plantillas de versión 2.
  
-   **Plantillas de certificado modificables:** las plantillas de la versión 1 no se pueden modificar o crear para generar nuevos tipos de certificado.
  
-   **No es compatible con el almacenamiento de claves**.
  
Si precisa alguna de estas características, necesitará una entidad emisora de certificados basada en las capacidades más avanzadas de la versión Enterprise Edition de Windows Server 2003. Para obtener una descripción minuciosa de las diferencias existentes entre Enterprise Edition y Standard Edition, consulte el documento "PKI Enhancements in Windows XP Professional and Windows Server 2003", incluido en la sección "Referencias" al final de este capítulo.
  
Si, por el contrario, actualmente no debe cumplir con requisitos establecidos en relación con otros tipos de certificados, podrá implementar la entidad emisora de certificados descrita en esta solución sin cerrar otras opciones en el futuro. De esta manera, si en una fase posterior identifica otros requisitos relativos a los certificados, podrá implementar una infraestructura de claves públicas más sofisticada. Esto le permitirá ejecutarlos conjuntamente o migrar para emitirlos todos desde la nueva infraestructura.
  
#### Clientes WLAN
  
La solución de WLAN es compatible con varios tipos distintos de clientes WLAN, ya sea de manera explícita o implícita. Asimismo, esta solución es compatible con clientes Windows XP, Professional Edition, Windows XP, Tablet Edition y Pocket PC 2003. Para obtener una orientación específica sobre el modo de configurar y usar estos clientes con la solución, consulte el capítulo 6, "Configuración de clientes de LAN inalámbricas". La guía no contempla el uso de otros tipos de clientes que admitan 802.1X con PEAP-MS-CHAP v2. Si bien algunos de estos tipos funcionarían (Windows 2000 Professional, por poner un ejemplo), la presente guía no contiene instrucciones sobre cómo configurarlos; además, el equipo de Microsoft Solutions for Security no ha realizado pruebas con ellos en esta solución.
  
#### Windows XP
  
Esta solución es plenamente compatible con Windows XP, Professional Edition y Windows XP, Tablet Edition. Todos los clientes Windows XP se deben actualizar con Service Pack 1 o posterior. Asimismo, los equipos deben ser miembros del mismo dominio que los servidores IAS o, al menos, miembros de otro dominio dentro del mismo bosque. La pertenencia a un dominio es necesaria para que los equipos se autentiquen en la WLAN y descarguen la configuración de WLAN especificada en la directiva de grupo.
  
La autenticación del equipo en la WLAN se emplea cuando ningún usuario ha iniciado sesión en él. De esta forma, el equipo podrá obtener la configuración del objeto de directiva de grupo, ejecutar secuencias de comandos de inicio y descargar revisiones. Esto también es necesario durante las primeras fases de inicio de sesión del usuario, ya que éste no podrá empezar la autenticación en WLAN hasta que se cargue su perfil. En consecuencia, se producirá un error en las secuencias de comandos de inicio de sesión, en otras configuraciones de objeto de la directiva de grupo y en los perfiles de itinerancia si el equipo no tiene una conexión existente con la red antes de que el usuario inicie sesión.
  
La solución puede usar equipos con Windows XP que no pertenezcan al dominio con las siguientes salvedades:
  
-   Deberá configurar el cliente WLAN manualmente.
  
-   La autenticación del equipo en WLAN no es fácil de obtener.
  
-   Para la autenticación del usuario en WLAN, el usuario deberá escribir sus credenciales de dominio (WLAN) en el cuadro de nombre de usuario y contraseña que aparezca.
  
Microsoft recomienda encarecidamente habilitar el servidor de seguridad personal en todos aquellos equipos cliente en los que se usen elementos inalámbricos.
  
#### Pocket PC 2003
  
Pocket PC 2003 es compatible con 802.1X y PEAP, si bien es posible que tenga que hacerse con actualizaciones del proveedor del dispositivo y de Microsoft para disfrutar de toda la funcionalidad de WLAN. Se pueden usar también versiones de Pocket PC anteriores a 2003, pero Microsoft no ha proporcionado compatibilidad integrada de 802.1X para versiones más antiguas. Es probable que pueda conseguir compatibilidad específica si se dirige al proveedor del dispositivo Pocket PC en cuestión, o bien si usa el software del cliente WLAN de otro fabricante.
  
Los sistemas Pocket PC no tienen un concepto de una cuenta de dominio de equipo y siempre se autentican en la WLAN por medio de las credenciales de usuario. Por lo general, un usuario debe escribir el nombre de usuario y la contraseña de dominio cada vez que quiera conectarse a la WLAN. Las credenciales se pueden guardar de manera que el dispositivo se conecte automáticamente, pero no es recomendable, a menos que se tengan unas características de seguridad muy sólidas en el dispositivo de Pocket PC.
  
Además, los Pocket PC no entienden el concepto de directiva de grupo, por lo que la configuración de WLAN no podrá establecerse de manera automática, sino manual.
  
#### Otros clientes 802.1X
  
Puede que algunos clientes que no son Windows XP ni Pocket PC 2003 funcionen con esta solución, siempre que sean compatibles con 802.1X y PEAP-MS-CHAP v2. Los clientes Windows 2000 son compatibles si se usa Microsoft 802.1X Authentication Client de Windows 2000. Los detalles sobre el modo de obtener Microsoft 802.1X Authentication Client de Windows 2000 se incluyen en las referencias recogidas al final del capítulo. Aquellos clientes de Windows que no sean Windows 2000 (así, Windows NT 4.0, Windows 9*x* y Windows Me) son compatibles con un cliente disponible a través de Microsoft Premier Support. Puede que obtenga un cliente para estas y otras plataformas de proveedores de software de red que no sean de Microsoft.
  
Consulte el apéndice C, "Versiones de sistemas operativos compatibles".
  
#### Compatibilidad con WPA
  
La solución de WLAN que aquí se describe admite el uso de la protección WPA en lugar de la WEP dinámica. WPA es siempre preferible a WEP, por cuanto ofrece una administración de claves más eficaz, al tiempo que implementa un algoritmo de cifrado de red más seguro. Asimismo, WPA admite el uso del cifrado de AES siempre que el hardware (puntos de acceso inalámbrico y adaptadores de red) proporcione la compatibilidad pertinente.
  
Si bien WPA proporciona un número de ventajas frente a la clave dinámica, hay una serie de puntualizaciones sobre su uso:
  
-   No se dispondrá de compatibilidad con el objeto de directiva de grupo para configurar WPA en clientes WLAN a menos que se tenga Windows Server 2003 Service Pack 1.
  
-   Es posible que el cliente sólo sea compatible con el sistema Windows XP. Si bien puede que Microsoft proporcione compatibilidad de WPA para Pocket PC 2003, es posible que no exista compatibilidad con Windows 2000 y otros clientes de Microsoft (algunos proveedores que no sean de Microsoft quizá proporcionen compatibilidad de WPA para estos clientes).
  
-   Puede que no sea posible actualizar el equipo de WLAN existente (puntos de acceso inalámbrico y adaptadores de red de los clientes) para que sea compatible con WPA. Asimismo, puede que el coste por adquirir e implementar el nuevo hardware sea muy elevado.
  
La compatibilidad del objeto de directiva de grupo y de Pocket PC 2003 con WPA tendrá lugar pronto (lo que hará de WPA una alternativa por la que decantarse), pero, hasta entonces, la WEP dinámica en uso conjunto con la autenticación 802.1X seguirá ofreciendo un nivel de protección muy elevado para las WLAN. Ésta es la elección predeterminada para esta solución. Para obtener más información sobre WPA, consulte la sección "Referencias" al final de este capítulo.
  
#### Migración desde una WLAN existente
  
Si ya tiene instalada una red inalámbrica, debe planear una estrategia de migración con antelación para garantizar que los usuarios y el entorno se vean afectados lo mínimo posible.
  
Muchas organizaciones tienen WLAN basadas en 802.11 que funcionan sin autenticación o cifrado de red, mientras que otras han implementado la WEP estática usando el cifrado de clave compartida combinado frecuentemente con el filtrado de direcciones de control de acceso de medios.
  
El proceso de migración de uno de estos escenarios a una WLAN protegida con 802.1X implica la consecución de los siguientes pasos:
  
1.  **Implementación de certificados para servidores IAS:** para obtener detalles sobre el modo de implementar certificados en un servidor IAS, consulte el capítulo 4 de esta guía, "Creación de la entidad emisora de certificados de red".
  
2.  **Configuración de las directivas de acceso remoto a redes inalámbricas en servidores IAS:** los pasos para configurar una directiva de acceso remoto inalámbrico se detallan en el capítulo 5 de esta guía, "Creación de la infraestructura de seguridad en LAN inalámbricas".
  
3.  **Implementación de una configuración de WLAN para los equipos cliente de la nueva WLAN nuevos:** la nueva red habilitada para 802.1X necesita un nuevo Identificador del conjunto de servicios de red. Así, la configuración de red para la nueva WLAN podrá implementarse mediante el objeto de directiva de grupo de Active Directory. La directiva de grupo de WLAN debe implementarse con suficiente antelación a la reconfiguración de los puntos de acceso inalámbrico para garantizar que los equipos móviles con acceso a LAN ocasional reciban la configuración. Esto se trata en el capítulo 6, "Configuración de clientes de LAN inalámbricas".
  
4.  **Configuración de puntos de acceso inalámbrico para que requieran la seguridad 802.1X:** por lo general, la mejor forma de llevar esto a cabo es sitio por sitio (por ejemplo, por edificios o por recintos) y ya sea fuera del horario laboral, o bien con el aviso correspondiente a los usuarios sobre una posible interrupción de la actividad de la WLAN. Deberá crear entradas de clientes RADIUS relacionados con IAS para todos los puntos de acceso inalámbrico del sitio, configurar los puntos de acceso con las direcciones de los servidores IAS para las entradas de RADIUS de los puntos de acceso y, finalmente, cambiar el punto de acceso para permitir únicamente a clientes autenticados con 802.1X. Puede que quiera hacer una copia de seguridad de la configuración de los puntos de acceso inalámbrico antes de iniciar este paso para que, en caso de emergencia, pueda recuperarse de forma sencilla.
  
Este modo de proceder provoca un trastorno menor en los usuarios, al tiempo que permite la recuperación de un sitio con facilidad en caso de que algo vaya mal. Es inevitable que, durante el cambio, los usuarios tengan que hacer frente a algún tipo de problema, de manera que es aconsejable mantenerlos convenientemente informados sobre la migración y, asimismo, deberá estar preparado para recibir más llamadas de soporte técnico de lo habitual.
  
Como sucede en todas las estrategias de migración, es esencial realizar un planeamiento y una comprobación precisos. Los pasos que implica la configuración de equipos cliente y puntos de acceso inalámbrico puede ocasionar cambios molestos en el entorno si no se prueba con detenimiento para resolver problemas incipientes.
  
El planeamiento detallado de la migración desde una WLAN insegura con WEP estática, o bien desde esquemas de seguridad de WLAN de propiedad, no se incluye en esta guía, ya que en principio son similares y siguen la pauta anterior. No obstante, si precisa de más asistencia para el planeamiento de la migración, consulte con su socio de Microsoft o bien póngase en contacto con la subsidiaria de Microsoft local, que, a su vez, le pondrá en contacto con un socio de Microsoft de su zona o con los Servicios de consultoría de Microsoft.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Escalabilidad para organizaciones más grandes
  
En esta sección se describen algunas de las consideraciones clave para el uso de esta solución en organizaciones de mayor volumen (una con miles de usuarios, por ejemplo). El uso de PEAP y de la autenticación mediante contraseña en la empresa se explica en el apéndice A, "Uso de PEAP en la empresa".
  
#### Colocación del servidor IAS
  
A medida que aumenta el número de ubicaciones donde se admiten las redes WLAN, necesitará decidir el modo en que los servidores IAS van a atender estos puntos de acceso inalámbrico. Existen dos enfoques fundamentalmente:
  
-   **Uso de un número reducido de servidores IAS centrales:** emplee un número pequeño de servidores IAS centrales para controlar todo el tráfico de autenticación en la WLAN (dos probablemente sería suficiente). Será necesario garantizar que las conexiones de WLAN entre oficinas remotas y los servidores IAS sean resistentes.
  
-   **Distribución de los servidores IAS en cada oficina:** el límite de tamaño de una oficina donde esto reporta beneficios económicos es más bajo, pero, como regla general, cualquier oficina que sea lo suficientemente grande como para tener controladores de dominio propios puede tener IAS de manera local (normalmente, instalado en el controlador de dominio).
  
La opción de invertir en la resistencia de la red puede parecer costosa, pero es necesario que la contraste con el coste de administración de los diversos servidores IAS distribuidos. Aun cuando IAS se halle instalado físicamente en el mismo servidor que un controlador de dominio existente, la administración de cada una de las instancias IAS supondrá un gasto. En la práctica, la mayoría de las grandes organizaciones emplearán un híbrido de ambas en alguna de las siguientes formas:
  
-   Centralización de los servidores IAS e inversión en resistencia de la WAN siempre que sea posible.
  
-   Distribución de IAS a oficinas donde no se puede disponer de resistencia de WAN o donde ésta es tremendamente costosa.
  
-   Uso de redes WLAN WPA de clave compartida previamente para oficinas muy pequeñas con escasa conectividad o para oficinas de aquellos empleados que trabajen desde casa.
  
La estrategia centralizada de IAS aparece reflejada en una sección anterior de este capítulo, "Colocación del servidor IAS". La siguiente figura muestra el uso de un controlador de dominio local y de IAS en una sucursal. Ésta contempla una oficina remota más grande vinculada, mediante WAN, a la oficina central de la figura 2.4. anterior.
  
[![](images/Dd162271.PEAP_207(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_207_big(es-es,technet.10).gif)
  
**Figura 2.7. Sucursal más grande con controlador de dominio local e IAS**
  
En este sitio, los puntos de acceso se configuran para usar el servidor IAS local como servidor RADIUS principal y uno de los servidores IAS de la oficina central, como servidor RADIUS secundario. Esto quiere decir que los clientes WLAN se pueden autenticar, incluso cuando se produzca un error en el servidor IAS local o en la conectividad WAN.
  
No obstante, si posee una conectividad WAN resistente (por ejemplo, varios vínculos WAN con proveedores distintos), apenas sacará partido de la implementación de servidores adicionales en las sucursales; de hecho, sólo agregará complejidad y más carga de administración.
  
#### Dominios múltiples
  
El diseño básico de la solución presenta una escala nítida con varios bosques de dominios. A continuación se exponen los puntos clave que se han de tener en cuenta al usar la solución con varios dominios:
  
-   Los servidores IAS deben registrarse en cada dominio que tenga usuarios y equipos que vayan a tener acceso a la WLAN. Para obtener detalles, consulte el capítulo 5, "Creación de la infraestructura de seguridad en LAN inalámbricas".
  
-   Los objetos de directiva de grupo para la configuración tanto del servidor como de la solicitud de certificados automática se deberán importar a todos los dominios en los que se instalen servidores IAS. Los pasos para llevar esto a cabo se explican en los capítulos 3, "Preparación del entorno" y 4, "Creación de la entidad emisora de certificados de red".
  
-   El objeto de directiva de grupo que controla la configuración de WLAN del equipo cliente debe crearse en cada dominio donde haya equipos cliente que vayan a tener acceso a la WLAN. Para obtener más detalles al respecto, consulte el capítulo 6, "Configuración de clientes de LAN inalámbricas".
  
-   Los grupos de seguridad que IAS utiliza para filtrar las directivas de acceso remoto deben configurarse a fin de admitir varios dominios.
  
Los tres primeros elementos no precisan más aclaración y, en cuanto a los pasos necesarios para configurarlos para dominios múltiples, se enumeran en capítulos posteriores. El tema del uso de los grupos de seguridad es algo más complejo y, como tal, se detalla en la siguiente sección.
  
#### Uso de grupos de seguridad en dominios múltiples
  
La siguiente tabla refleja el modo en que los grupos de seguridad descritos en la sección "Modelo de administración de usuario y equipo de WLAN" se pueden organizar dentro de un bosque con varios dominios.
  
**Tabla 2.8. Grupos de acceso inalámbrico para permitir a todos los usuarios y equipos**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupo universal de nivel superior (acceso concedido en la directiva de acceso remoto)</th>
<th style="border:1px solid black;" >Miembros de primer nivel
(grupos globales de dominio)</th>
<th style="border:1px solid black;" >Miembros de segundo nivel
(globales de dominio)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">DomRa\Acceso a LAN inalámbrica</td>
<td style="border:1px solid black;">DomUsuario1\Usuarios de LAN inalámbrica</td>
<td style="border:1px solid black;">DomUsuario1\Usuarios de dominio</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">DomRa\Acceso a LAN inalámbrica</td>
<td style="border:1px solid black;">DomUsuario2\Usuarios de LAN inalámbrica</td>
<td style="border:1px solid black;">DomUsuario2\Usuarios de dominio</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">DomRa\Acceso a LAN inalámbrica</td>
<td style="border:1px solid black;">DomUsuario3\Usuarios de LAN inalámbrica</td>
<td style="border:1px solid black;">DomUsuario3\Usuario1<br />
DomUsuario3\Usuario2<br />
DomUsuario3\Usuario2</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">DomRa\Acceso a LAN inalámbrica</td>
<td style="border:1px solid black;">DomUsuario1\Equipos de LAN inalámbrica</td>
<td style="border:1px solid black;">DomUsuario1\Equipos de dominio</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">DomRa\Acceso a LAN inalámbrica</td>
<td style="border:1px solid black;">DomUsuario2\Equipos de LAN inalámbrica</td>
<td style="border:1px solid black;">DomUsuario2\Equipos de dominio</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">DomRa\Acceso a LAN inalámbrica</td>
<td style="border:1px solid black;">DomUsuario3\Equipos de LAN inalámbrica</td>
<td style="border:1px solid black;">DomUsuario3\Equipos de recursos humanos<br />
DomUsuario3\Equipos de finanzas</td>
</tr>
</tbody>
</table>
 

Esta tabla refleja la misma disposición de grupos anidados que las tablas de la sección "Modelo de administración de usuario y equipo de WLAN". Los miembros de los grupos recogidos en la primera columna aparecen en la segunda columna y los de los grupos enumerados en la segunda columna, en la tercera.

El ejemplo de la tabla emplea nombres ficticios. Así, DomRa es el nombre del dominio en el que se instalan los servidores IAS, mientras que DomUsuario1 y DomUsuario2 hacen referencia a otros dominios que contienen usuarios y equipos a los que se concede acceso a WLAN.

En el ejemplo, todos los usuarios y equipos de DomUsuario1 y DomUsuario2 obtienen acceso a la WLAN de forma implícita, por cuanto los usuarios y los equipos de dominio de tales dominios pertenecen a los grupos de usuarios y de equipos de LAN inalámbricas para el mismo dominio. Sin embargo, los usuarios de DomUsuario3 se agregan de manera individual a los grupos de usuarios de la LAN inalámbrica de DomUsuario3. Los equipos obtienen acceso mediante los grupos de seguridad de unidad comercial (por ejemplo, todos los equipos en el departamento de recursos humanos).

Los grupos globales para cada dominio (esto es, para usuarios de LAN inalámbrica y equipos de LAN inalámbrica) se agregan como miembros del grupo universal de acceso a LAN inalámbrica. Todos los miembros de este último grupo obtienen acceso a WLAN en la directiva de acceso remoto de IAS.

#### Arquitectura de infraestructura de claves públicas

Tal y como se menciona en la sección anterior "Obtención de certificados para servidores IAS", una gran parte de las aplicaciones usan certificados. Es importante resaltar que, si bien es adecuada para esta solución, es posible que una entidad emisora de certificados independiente no cubra las necesidades de organizaciones más grandes por ser más diversas. Así, antes de implementar la entidad emisora descrita en esta guía, sopese con detenimiento el uso de otros certificados que pueda tener en el futuro, así como de otras arquitecturas de infraestructura de claves públicas alternativas que se adecuen de mejor forma a estos escenarios.

Para obtener información detallada sobre el planeamiento de la infraestructura de claves públicas, consulte el capítulo 4, "Diseño de la infraestructura de claves públicas", de la solución complementaria, *Solución de Seguridad de LAN inalámbricas — Servicios de Certificate Server de Microsoft Windows Server 2003*. Aun siendo más sofisticada que la entidad emisora de certificados de esta guía, la infraestructura de claves públicas tratada en esa solución sigue siendo relativamente sencilla (sólo usa dos entidades emisoras de certificados, por ejemplo). No obstante, se ha diseñado para que constituya la base de un intervalo mucho más amplio de necesidades de certificado.

Si decide implementar una infraestructura de claves públicas más sofisticada (como ésta), podrá tomar como referencia las indicaciones del capítulo 4 de esta guía, "Creación de la entidad emisora de certificados de red". De todas formas, no olvide que debe aplicar los siguientes cambios en las instrucciones que ese capítulo contempla:

-   Instale la entidad emisora de certificados en su propio servidor y no en un controlador de dominio.

-   Utilice la versión Enterprise Edition de Windows Server 2003 a fin de poder disfrutar de una mayor flexibilidad en el futuro.

-   En lugar de usar el servicio de solicitud de certificados automática, emplee la inscripción automática de Windows Server 2003. Para obtener instrucciones sobre el modo de usar la inscripción automática, consulte la documentación de producto de Windows Server 2003 Enterprise Edition.

-   Use la plantilla de certificado "Servidor RAS e IAS", o bien cree un tipo de certificado de cliente para los certificados del servidor IAS en lugar de usar la plantilla "Equipo".

    **Nota:** "RAS" en la plantilla de certificados corresponde al inglés *Remote Access Service* (servicio de acceso remoto).

Podrá obtener más indicaciones al respecto en la sección sobre la infraestructura de claves públicas de la documentación de producto de Windows Server 2003, así como en el capítulo 4 ("Diseño de la infraestructura de claves públicas"), el capítulo 7 ("Implementación de la infraestructura de claves públicas") y el capítulo 9 ("Implementación de la seguridad de LAN inalámbricas mediante 802.1X") de la solución complementaria, *Solución de Seguridad de LAN inalámbricas — Servicios de Certificate Server de Microsoft Windows Server 2003*.

[](#mainsection)[Principio de la página](#mainsection)

### Variaciones en la arquitectura de la solución

En esta sección se tratan las variaciones que pueden producirse en el diseño básico. Las siguientes subsecciones se centran en las alternativas de configuración de seguridad de la solución, como usar los servidores IAS para la autenticación de acceso remoto y con cable, crear WLAN de invitado para visitantes e implementar WLAN en entornos muy pequeños, como oficinas en casa.

#### Opciones de seguridad para la WEP dinámica

La sección anterior, "Funcionamiento de 802.1X con PEAP y contraseñas", trata del uso del cifrado de la WEP dinámica en esta solución. La seguridad de la WEP dinámica se basa en su capacidad para renovar las claves de cifrado de manera periódica y, de este modo, frustrar ataques conocidos en el protocolo de WEP. IAS garantiza que las claves de cada uno de los clientes inalámbricos se van a renovar en un intervalo establecido mediante el tiempo de espera de la sesión del cliente, que obliga al cliente a volver a autenticarse en la WLAN.

La reducción del valor del tiempo de espera de sesión aumenta la seguridad, pero, al mismo tiempo, puede mermar la confiabilidad y el rendimiento. Un tiempo de espera de 60 minutos proporciona la seguridad apropiada en la mayoría de las circunstancias y, por supuesto, también para las redes 802.11b de 11 Mbps. Por lo general, los clientes inalámbricos nunca van a transferir datos suficientes en 60 minutos como para permitir que un atacante obtenga la clave WEP.

Las últimas investigaciones arrojan que las claves WEP estáticas pueden obtenerse mediante la captura de entre 1 y 5 millones de paquetes de red cifrados con la misma clave. Esto se recoge en el documento técnico "Using the Fluhrer, Mantin, and Shamir Attack to Break WEP" de Adam Stubblefield, John Ioannidis y Aviel D. Rubin de AT&T Labs, consulte las referencias al final de este capítulo.

**Nota:** la cifra de 1 millón de paquetes se ha obtenido de la comprobación de WLAN de WEP usando claves relativamente débiles (una "frase fácil de memorizar") y, por lo tanto, no se puede aplicar directamente a las WLAN de WEP dinámica. Al contrario de lo que sucede con las WLAN de WEP estática, la WEP dinámica emplea claves de cifrado aleatorio seguras y resta gran parte de la eficacia de las optimizaciones de clave que los autores utilizan. De todas formas, acostúmbrese a equivocarse como hábito de seguridad y a usar la cifra de 1 millón de paquetes para evaluar la amenaza sobre la seguridad en las WLAN de WEP dinámica.

Un millón de paquetes normalmente equivalen a alrededor de 500 MB de datos (suponiendo que el tamaño medio de un paquete sea de 500 bytes). A fin de que los datos cifrados estén protegidos, el tiempo de espera de sesión habrá de establecerse de manera que obligue a renovar la clave del cliente antes de que se envíe una cantidad de datos superior a la indicada.

En cuanto al uso típico de la red por parte del cliente (como correo electrónico, explorar el Web o compartir archivos), la media de velocidad de transferencia de archivos es de 160 Kbps o inferior. A esta velocidad, y suponiendo que el tamaño de un paquete es de 500 bytes, un atacante tardaría aproximadamente 7 horas en acumular la información suficiente como para dar con la clave de cifrado actual del cliente.

**Nota:** en el entorno de un laboratorio, se invertiría mucho menos de 7 horas en transferir 500 Mb (unos 10 minutos en una red WLAN a 11 Mbps o menos de 3 minutos en una WLAN a 54 Mbps). Sin embargo, aquí se da por hecho que un solo cliente disfruta de uso exclusivo de la WLAN y transfiere paquetes UDP o autorizados en una dirección, situación que difícilmente se produciría en una WLAN del mundo real.

Un tiempo de espera de sesión de 60 minutos es más que suficiente para la mayoría de las organizaciones. Esto indica que un cliente transferiría un promedio de 150.000 paquetes antes de que cada clave se actualizara; es decir, un pedido de aproximadamente una magnitud inferior al umbral de 1 millón de paquetes necesario para hacerse con la clave WEP. No obstante, es posible que quiera disfrutar de un valor de tiempo de espera más breve por una o varias de las siguientes razones:

-   Si tiene clientes inalámbricos que envían o reciben grandes cantidades de datos a través de la WLAN en períodos de tiempo relativamente cortos, debería establecer un tiempo de espera con una duración menor que el tiempo que tarda un solo cliente en enviar y recibir 75 MB (que corresponde a menos del 20 por ciento de la cantidad de datos necesaria para conseguir la clave WEP, por lo que el margen de seguridad es amplio).

-   Si utiliza WLAN 802.11a o WLAN 802.11g de 54 Mbps, resulta más fácil transferir un mayor número de paquetes en un tiempo determinado. En este tipo de WLAN de mayor velocidad, es posible que desee reducir el tiempo de espera de sesión a 15 minutos.

-   Si las técnicas para descifrar la clave WEP mejoran de manera muy considerable, la cantidad de datos necesaria para obtener las claves WEP será menor. Así, si surge una nueva técnica analítica de cifrados que permite obtener claves con tan solo 100.000 paquetes, deberá reducir el tiempo de espera de sesión a fin de evitar que los clientes inalámbricos alcancen este límite antes de que las claves de cifrado se renueven.

-   Si tiene necesidades de seguridad de especialista, posiblemente quiera establecer este tiempo por debajo del umbral en el que incluso los ataques teóricos de WEP serían fructíferos (10 minutos o 3 minutos, tal y como se ha señalado en la nota anterior). De todas formas, medite esta decisión teniendo presente las salvedades expuestas más adelante en esta sección. En caso de que los datos sean lo suficientemente confidenciales como para fijar este nivel de precaución, debería considerar seriamente el uso exclusivo de la protección de datos WPA en la WLAN y usar la seguridad IP como ayuda para la protección de los datos cuando fluyen por las LAN con cable.

Existen principalmente dos inconvenientes a la hora de reducir el tiempo de espera de sesión:

-   **Peor confiabilidad** **de la WLAN:** un tiempo de espera de sesión en WLAN de escasa duración podría provocar errores en la reautenticación y la desconexión de la propia red en caso de que la comunicación con un controlador de dominio o un servidor IAS se perdiera de manera temporal.

-   **Aumento de la carga en los servidores IAS:** cuanto más breve sea el tiempo de espera, más veces tendrá que volver a autenticarse el usuario con un servidor IAS y un controlador de dominio, de manera que la carga en éstos incrementará. Dado que IAS almacena en caché las sesiones de autenticación del cliente, normalmente este aumento de la carga será significativo sólo en aquellas organizaciones con un gran número de clientes inalámbricos o al utilizar valores de tiempo de espera de sesión de muy poca duración.

#### Otros servicios de acceso a la red

El diseño de RADIUS utilizado en esta solución puede proporcionar servicios de autenticación, autorización y contabilidad para otros servidores de acceso a la red como la autenticación de red 802.1X con cable y la autenticación de acceso remoto y VPN.

#### Autenticación de red por cable 802.1X

La autenticación de red por cable 802.1X constituye la aplicación más sencilla que no precisa modificación alguna del diseño básico de RADIUS. Es posible que las organizaciones que tienen una infraestructura de red por cable de amplia distribución encuentren difícil controlar el uso no autorizado de la red corporativa. Por ejemplo, normalmente es difícil impedir que los visitantes conecten equipos portátiles o que los empleados agreguen equipos no autorizados a la red. Algunas secciones de la red, como los centros de datos, pueden tener designadas zonas de alta seguridad, de manera que sólo los dispositivos autorizados deben admitirse en estas redes. Esto supondría la exclusión, si procediera, de empleados con equipos corporativos.

En la siguiente figura se ilustra cómo una solución de acceso a red por cable se integraría con el diseño.

[![](images/Dd162271.PEAP_208(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_208_big(es-es,technet.10).gif)

**Figura 2.8. Uso de la autenticación por cable 802.1X**

El cuadro con los bordes resaltados representa los componentes por cable 802.1X, mientras que los otros contienen los servicios relevantes. Compare esta figura con la figura 2.4. En esta figura sólo se muestra la oficina central.

Los conmutadores de red que admiten 802.1X tienen una función idéntica a los puntos de acceso inalámbrico en la solución principal y pueden utilizar la misma infraestructura de RADIUS para autenticar clientes y autorizar selectivamente el acceso al segmento de red correspondiente. Esto proporciona las ventajas obvias de centralizar la administración de cuentas en el directorio corporativo, pero manteniendo las directivas de acceso a la red bajo el control del administrador de seguridad de la red.

#### Autenticación de VPN y acceso telefónico remoto

Otro servicio de acceso a la red que podría utilizar los componentes RADIUS es la VPN y el acceso telefónico remoto. Es probable que, particularmente en las organizaciones grandes, sea necesario agregar algunos elementos al diseño original, como servidores proxy RADIUS. La siguiente figura refleja la solución ampliada.

[![](images/Dd162271.PEAP_209(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_209_big(es-es,technet.10).gif)

**Figura 2.9. Extensión del componente RADIUS para admitir VPN**

Los servidores VPN de esta variante cumplen la misma función que los puntos de acceso inalámbrico en el diseño principal: pasar las solicitudes de autenticación de los clientes a la infraestructura de RADIUS. Las solicitudes de RADIUS se pueden pasar directamente a los servidores IAS internos. No obstante, muchas organizaciones optan por agregar un nivel adicional de servidores proxy RADIUS para que proporcione un nivel de seguridad extra y para que las solicitudes se enruten a los servidores IAS internos.

En lo que se refiere a la seguridad de la red con cable, esta solución aporta las mismas ventajas de reutilización de la infraestructura existente y de centralización de la administración de cuentas. Existen otras mejoras, como el uso de la autenticación de usuarios basada en tarjetas inteligentes. La solución de VPN de acceso remoto interna de Microsoft para el propio personal de la empresa utiliza virtualmente la misma VPN y la misma arquitectura de RADIUS con tarjetas inteligentes para la autenticación de usuarios.

El acceso telefónico remoto funciona de manera similar mediante la utilización de la capacidad de servidor de acceso telefónico en lugar de las funciones de VPN del Servicio de enrutamiento y acceso remoto de Windows.

La principal ventaja que el uso de IAS ofrece a VPN y al acceso remoto consiste en la capacidad para utilizar la característica de control de cuarentena para acceso a la red de Windows Server 2003. El control de la cuarentena emplea capacidades de los servidores de enrutamiento y acceso remoto (RAS) y del cliente de acceso remoto mejorado de Windows (Connection Manager) para permitir y denegar el acceso en función del estado de seguridad del equipo cliente. Esto se lleva a cabo realizando comprobaciones en el cliente cuando éste se conecta, y así, para garantizar que dispone de un software antivirus actualizado o que utiliza una versión aprobada del sistema operativo corporativo. En caso de que el cliente no supere estas comprobaciones, el servidor RADIUS le denegará el acceso a la red. Por eso, se puede denegar el acceso a un usuario y un equipo autorizados adecuadamente si representan una amenaza de seguridad para la red de la compañía.

Para obtener más información sobre la característica de cuarentena de Windows Server 2003, consulte las referencias al final de este capítulo.

#### Inicio de equipos cliente

La mayoría de los equipos con capacidades inalámbricas cuentan también con una interfaz de red con cable, dado que así se facilita en cierta medida que los clientes puedan unirse al dominio y descarguen la configuración de WLAN antes de conectarse a ésta. Sin embargo, no siempre va a producirse esta situación. Ya existen dispositivos de mano que son inalámbricos en su totalidad y, por lo tanto, no tienen adaptadores de red con cable. Esto supone el inconveniente de iniciar un cliente antes de que se conecte a la WLAN, por cuanto no posee la configuración ni las credenciales necesarias para conectarse a ella.

Este problema se agrava si en una organización decide usarse la seguridad 802.1X tanto inalámbrica como con cable, ya que un cliente no puede conectarse a una LAN con cable sin poseer las credenciales y la configuración pertinentes.

Existen dos enfoques fundamentales para iniciar un equipo cliente si no se puede usar una LAN con cable para obtener la configuración y credenciales:

-   Uso de una LAN de invitado y de otra conexión autenticada (por ejemplo, una conexión de VPN) para obtener las credenciales y la configuración.

-   Configuración manual de los clientes.

Actualmente, Microsoft sólo admite la segunda opción, si bien va a lanzar un servicio de disposición inalámbrica que permitirá el uso de una WLAN "de invitado" con la que iniciar la configuración de la WLAN del equipo cliente. Hasta entonces, la configuración manual constituye un modo sencillo de llevar esto a cabo. Para configurar el equipo cliente y unirlo al dominio, la persona responsable de ello debe pertenecer al grupo Administradores local del equipo.

**Para iniciar un equipo mediante la configuración manual:**

1.  Configure manualmente la WLAN para el SSID de WLAN correspondiente.

2.  Conecte la WLAN utilizando credenciales de dominio de usuario válidas. No podrá conectarse mediante la cuenta de equipo hasta que el equipo no se haya unido al dominio.

3.  Una el equipo al dominio y, a continuación, reinícielo.

4.  Tras ello, el cliente podrá conectarse a la WLAN usando la cuenta de equipo y, por lo tanto, podrá descargar la configuración del objeto de directiva de grupo de la WLAN. Esta configuración simplemente se sobrescribirá sobre la ya establecida manualmente.

5.  Llegado este momento, tanto el usuario como el equipo podrán conectarse a la WLAN.

#### Entorno SOHO

Puede que tenga que implementar las WLAN en ubicaciones donde no es posible (o no resulta práctico) autenticar usuarios por medio de la infraestructura de IAS; así, por ejemplo, en oficinas domésticas de aquellos usuarios que trabajan habitualmente en casa, o bien en oficinas pequeñas con una conectividad a la red corporativa principal baja y poco confiable.

Antes, la única salida a esto consistía en configurar la seguridad de WEP estática y cruzar los dedos para que nadie pusiera demasiado empeño en atacar la WLAN. Por ello, una solución mucho más eficaz consiste en usar WPA en modo de infraestructura de claves públicas. Todos los puntos de acceso inalámbrico con certificado Wi-Fi llevan ahora incorporada la seguridad WPA, si bien es probable que algunos puntos de acceso más antiguos no sean compatibles con ella. Debe asegurarse de que los puntos de acceso son compatibles con WPA de clave previamente compartida por el valor de seguridad adicional que ésta ofrece. Al contrario de lo que sucede con WEP, la clave de autenticación de WPA no puede obtenerse del tráfico cifrado; en consecuencia, resultará mucho más difícil para un atacante irrumpir en la red. Asimismo, deberá garantizar que los usuarios cuentan con los conocimientos necesarios para utilizar claves de WPA seguras y para cambiarlas de manera periódica y, al mismo tiempo, asegurarse de que son conscientes de las implicaciones de seguridad que esto conlleva. Para implementar WPA de clave previamente compartida, necesita un punto de acceso inalámbrico, adaptadores de red inalámbricos y un sistema operativo cliente (como Windows XP) que sea compatible con WPA. No es necesario tener un servidor RADIUS o cualquier otro tipo de infraestructura de servidores.

[](#mainsection)[Principio de la página](#mainsection)

### Resumen

Este capítulo ha comenzado con una descripción del modo en que la seguridad en las LAN inalámbricas 802.1X funciona. En aras de centrarse en el diseño, se ha proporcionado una imagen de la organización de destino para la solución, así como los criterios de diseño clave de la organización para la solución de WLAN. A partir de estos elementos, se ha pasado a tratar los aspectos principales del diseño de WLAN escogido. Este diseño ha incluido la red, la colocación del servidor IAS y la configuración de IAS, el uso de certificados y los distintos tipos de clientes inalámbricos. Asimismo, se han expuesto los puntos clave de la migración desde una WLAN existente.

En las dos últimas secciones al final del capítulo se han recogido las variaciones más relevantes que pueden darse en el diseño básico de la solución. Primero, se ha descrito el modo de dotar a la solución de escalabilidad para organizaciones más grandes, junto con instrucciones sobre el modo de afrontar los principales puntos de divergencia de la solución central; Tras ello, se han incluido ilustraciones sobre el modo de usar la misma infraestructura de autenticación básica para admitir otros servicios de red como el acceso remoto, VPN y la seguridad de red con cable, y, por último, se ha detallado el modo de solucionar problemas bastante incómodos de inicio de clientes y de implementación de WLAN en entornos SOHO.

El capítulo siguiente comienza con la implementación de la solución a través de la preparación de la red, Active Directory, y la seguridad de servidores para implementar componentes de WLAN.

[](#mainsection)[Principio de la página](#mainsection)

### Referencias

Esta sección ofrece referencias a otra información complementaria importante u otro material informativo de relevancia para el contenido de este capítulo.

-   Para obtener más detalles sobre la autenticación 802.1X, consulte "IEEE 802.1X Authentication for Wireless Connections" en la siguiente dirección URL:

    [http://www.microsoft.com/technet/columns/cableguy/cg0402.mspx](http://technet.microsoft.com/es-es/library/bb878016.aspx)

-   Para obtener más información sobre el modo en que PEAP funciona con contraseñas, consulte "PEAP with MS-CHAP Version 2 for Secure Password-based Wireless Access" en la siguiente dirección URL:

    [http://www.microsoft.com/technet/columns/cableguy/cg0702.mspx](http://technet.microsoft.com/es-es/library/bb878077.aspx)

-   Para obtener información sobre la autenticación 802.1X, la interacción entre clientes, los puntos de acceso inalámbrico y los servidores RADIUS, así como recomendaciones relativas a las funciones que deberían ser compatibles con los puntos de acceso, consulte "Recommendations for IEEE 802.11 Access Points" en la siguiente dirección URL:

    [http://www.microsoft.com/whdc/hwdev/tech/network/802x/AccessPts.mspx](http://www.microsoft.com/whdc/archive/accesspts.mspx)

-   Para obtener más información sobre el diseño de la LAN inalámbrica, incluidos los servicios DHCP y la distribución de los puntos de distribución, consulte el capítulo sobre la implementación de una LAN inalámbrica del *Kit de distribución de Microsoft Windows Server 2003* en la siguiente dirección URL:

    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs
    /deployguide/DNSBM\_WIR\_OVERVIEW.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/deployguide/dnsbm_wir_overview.mspx)

-   Para obtener más información sobre la protección de IAS, consulte la documentación de producto de Windows Server 2003 en la siguiente dirección URL:

    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs
    /standard/sag\_ias\_security.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/standard/sag_ias_security.mspx)

-   Para obtener más información sobre las características de Servicios de Certificate Server disponibles en la versión Enterprise Edition de Windows Server 2003, consulte el documento "PKI Enhancements in Windows XP Professional and Windows Server 2003" en la siguiente dirección URL:

    <http://www.microsoft.com/technet/prodtechnol/winxppro/plan/pkienh.mspx>

    **Nota:** la redacción de este artículo se realizó antes del lanzamiento de Windows Server 2003, de manera que en él se hace uso de los términos Windows .Net Server, Advanced Server y Standard Server donde debería decirse Windows Server 2003, Enterprise Edition y Standard Edition respectivamente.

-   Para obtener más información sobre Microsoft 802.1X Authentication Client para Windows 2000, consulte el artículo de la Knowledge Base "Using 802.1x Authentication on Computers Running Windows 2000" en la siguiente dirección URL:

    <http://support.microsoft.com/default.aspx?scid=313664>

-   Para obtener más información sobre "Wi-Fi Protected Access (WPA) Overview" y la "Introducción a la actualización de seguridad de WPA inalámbrico en Windows XP", consulte las siguientes direcciones respectivamente:

    [http://www.microsoft.com/technet/columns/cableguy/cg0303.mspx](http://technet.microsoft.com/es-es/library/bb877996.aspx)

    <http://support.microsoft.com/default.aspx?scid=kb;es;815485>

-   Para conocer los asuntos de seguridad relacionados con WEP, consulte los documentos técnicos "Weaknesses in the Key Scheduling Algorithm of RC4" de Scott Fluhrer, Itsik Mantin y Adi Shamir y "Using the Fluhrer, Mantin, and Shamir Attack to Break WEP" de Adam Stubblefield, John Ioannidis y Aviel D. Rubin. Tenga presente que en estos documentos se trata la seguridad de la WEP estática y que, por lo tanto, las conclusiones que en ellos se arrojan no son directamente aplicables a las WLAN de WEP dinámica. Para el primer documento, consulte la siguiente dirección:

    <http://www.crypto.com/papers/others/rc4_ksaproc.pdf>

-   Para obtener más información sobre la implementación de LAN inalámbricas y VPN de acceso remoto en Microsoft, consulte "Mobility: Empowering People through Wireless Networks" y "Securing Remote Users at Microsoft" en las siguientes direcciones:

    [http://www.microsoft.com/technet/itsolutions/msit/security/secwlan.mspx](http://technet.microsoft.com/en-us/solutionaccelerators/cc835245.aspx)

    [http://www.microsoft.com/resources/casestudies/
    casestudy.asp?casestudyid=13787](http://www.microsoft.com/resources/casestudies/casestudy.asp?casestudyid=13787)

-   Para obtener más información sobre el control de cuarentena para acceso a la red, consulte los documentos "Network Access Quarantine Control in Windows Server 2003" y "Planning for Network Access Quarantine Control" en las siguientes direcciones:

    [http://support.microsoft.com/default.aspx?scid=818747](http://technet.microsoft.com/en-us/library/cc786745.aspx)

    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/deployguide/dnsbf_vpn_aosh.mspx)
    [/deployguide/dnsbf\_vpn\_aosh.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/deployguide/dnsbf_vpn_aosh.mspx)

-   Para obtener más información sobre el uso de WPA para proteger las WLAN en entornos SOHO, consulte "WPA Wireless Security for Home Networks" en la siguiente dirección URL:

    [http://www.microsoft.com/WindowsXP/expertzone/columns/bowman/03july28.asp](http://www.microsoft.com/windowsxp/expertzone/columns/bowman/03july28.asp)

(Este artículo contiene referencias a guías de otros productos y vínculos a sitios Web que sólo están disponibles en inglés.)

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 3: Preparación del entorno

[](#ejaa2)[Información general](#ejaa2)
[](#eiaa2)[Requisitos previos del capítulo](#eiaa2)
[](#ehaa2)[Requisitos previos y supuestos de la infraestructura de TI](#ehaa2)
[](#egaa2)[Preparación de la implementación](#egaa2)
[](#efaa2)[Instalación de herramientas de la solución](#efaa2)
[](#eeaa2)[Configuración de la infraestructura de directorio y de red](#eeaa2)
[](#edaa2)[Preparación de los servidores](#edaa2)
[](#ecaa2)[Resumen](#ecaa2)
[](#ebaa2)[Referencias](#ebaa2)

### Información general

Este capítulo ayuda a preparar el entorno de tecnología de la información (TI) para implementar la infraestructura de seguridad para su red de área local inalámbrica (WLAN). Las principales tareas para preparar el entorno incluyen:

-   Preparar el dominio del servicio de directorio Microsoft® Active Directory® creando grupos de seguridad necesarios.

-   Preparar sus servidores para instalar el Servicio de autenticación de Internet (IAS) y los Servicios de Certificate Server. Esta tarea también incluye las tres subtareas siguientes:

    -   Aplicar configuración de seguridad a los servidores.

    -   Instalar herramientas necesarias en los servidores.

    -   Actualizar los servidores para garantizar que no tienen vulnerabilidades de seguridad.

[](#mainsection)[Principio de la página](#mainsection)

### Requisitos previos del capítulo

Antes de continuar, debe tener un buen conocimiento de la arquitectura y el diseño de esta solución que se describe en el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas". Además, debe estar familiarizado con la instalación y administración de Microsoft Windows® 2000 Server o Microsoft Windows Server™ 2003. También puede ser útil el conocimiento de los siguientes temas:

-   Conceptos de Active Directory, incluyendo estructura y herramientas de administración, administración de usuarios, grupos y otros objetos de Active Directory y utilización de la directiva de grupo.

-   Temas relacionados con la seguridad del sistema Windows, incluyendo conceptos de seguridad como usuario y grupos, auditoría de las listas de control de acceso (ACL) y aplicación de configuración de seguridad mediante la directiva de grupo.

-   Lenguaje Windows Scripting Host y Microsoft Visual Basic® Scripting Edition (VBScript).

[](#mainsection)[Principio de la página](#mainsection)

### Requisitos previos y supuestos de la infraestructura de TI

Este capítulo y los siguientes de esta guía se basan en los siguientes supuestos sobre infraestructura de TI, aunque algunos se pueden implementar como parte de esta solución. Muchos de estos supuestos no son requisitos rígidos; en esta guía se indica dónde hay configuraciones alternativas válidas.

-   Un bosque de Active Directory con controladores de dominio Windows 2000 Server o Windows Server 2003, con todos los usuarios de WLAN como miembros de un dominio en el mismo bosque.

    **Nota:** los controladores de dominio en los que se instalan IAS y los Servicios de Certificate Server deben ejecutar Windows Server 2003.

-   Dos o más servidores ejecutando Windows Server 2003, Standard Edition (Windows Server 2003, Enterprise Edition también es compatible) en los que se instalan componentes de la solución.

-   Estos servidores tienen capacidad suficiente para ejecutar IAS y Servicios de Certificate Server, además de cualquier servicio y aplicación existente. Los Servicios de Certificate Server se instalan sólo en el servidor principal.

-   IAS se instalará en controladores de dominio existentes. Esto es opcional ya que puede instalar IAS en un servidor miembro de dominio.

-   Los Servicios de Certificate Server se instalarán en un controlador de dominio. De forma opcional, puede instalar Servicios de Certificate Server en un servidor miembro de dominio.

-   Tiene acceso al medio de instalación de Windows Server 2003.

-   El dominio en el que se instalará IAS se está ejecutando en el modo nativo de Windows 2000. Esto es opcional.

-   Una infraestructura LAN inalámbrica instalada o planeada que conste de varios puntos de acceso inalámbrico. El diseño de la infraestructura de WLAN y los temas relacionados, como la colocación de los puntos de acceso inalámbrico y la selección de canal no se tratan en esta guía.

-   Se asume que la organización en su totalidad tiene menos de 50 puntos de acceso.

-   Una o más sucursales sin controladores de dominio local (y sin servidores IAS) pero con clientes que necesitan conexiones a la WLAN.

Aunque la solución se ha creado para este perfil específico, el diseño básico se puede adaptar a muchas otras configuraciones, como sucursales con controladores de dominio local o la instalación en bosques de varios dominios. El impacto de las configuraciones alternativas válidas, cuando sea aplicable, se describe en esta guía.

[](#mainsection)[Principio de la página](#mainsection)

### Preparación de la implementación

#### Permisos necesarios

Para llevar a cabo los procedimientos indicados en este capítulo debe utilizar una cuenta miembro del grupo Administradores para el dominio que contiene los servidores. De forma predeterminada, la cuenta de administrador integrada del dominio es miembro del grupo Administradores, aunque puede utilizar cualquier otra cuenta que pertenezca al grupo.

**Nota:** esta guía se basa en la suposición de que está instalando Servicios de Certificate Server e IAS en un controlador de dominio. Si los está instalando en servidores que no son controladores de dominio, la cuenta que utilice sólo necesitará ser miembro del grupo Administradores local en cada uno de los servidores.

#### Herramientas necesarias

Necesita las siguientes herramientas para llevar a cabo los procedimientos descritos en este capítulo:

**Tabla 3.1. Herramientas necesarias**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Herramienta</th>
<th style="border:1px solid black;" >Descripción</th>
<th style="border:1px solid black;" >Fuente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Secuencias de comandos de solución WLAN</td>
<td style="border:1px solid black;">Conjunto de secuencias de comandos y herramientas proporcionado con esta solución.</td>
<td style="border:1px solid black;">Los detalles de instalación se proporcionan en este capítulo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Consola de administración de directivas de grupo</td>
<td style="border:1px solid black;">Herramienta de administración avanzada de objetos de directiva de grupo que permite importarlos y exportarlos.</td>
<td style="border:1px solid black;">Se puede descargar del sitio Microsoft.com.<br />
Los detalles de instalación se proporcionan en este capítulo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">CAPICOM</td>
<td style="border:1px solid black;">Biblioteca del sistema que permite ejecutar secuencias de comandos de operaciones de certificado y seguridad.</td>
<td style="border:1px solid black;">Se puede descargar del sitio Microsoft.com.<br />
Los detalles de instalación se proporcionan en este capítulo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><em>DSACLs.exe</em></td>
<td style="border:1px solid black;">Herramienta de línea de comandos, que permite establecer permisos en los objetos de Active Directory.</td>
<td style="border:1px solid black;">CD de instalación de Windows Server 2003.<br />
Los detalles de instalación se proporcionan en este capítulo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Usuarios y equipos de Active Directory</td>
<td style="border:1px solid black;">Herramienta de Microsoft Management Console (MMC) utilizada para administrar usuarios, grupos, equipos y otros objetos de Active Directory.</td>
<td style="border:1px solid black;">Instalado como parte de Windows Server 2003.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Instalación de herramientas de la solución
  
Con esta guía se proporcionan una serie de secuencias de comandos y herramientas para ayudar a simplificar la configuración y el funcionamiento de esta solución. Debe instalar estas secuencias de comandos y herramientas en cada uno de los servidores IAS. Algunas de estas secuencias de comandos son necesarias durante las operaciones en curso (como se describe en el capítulo 8, "Mantenimiento de soluciones de seguridad en LAN inalámbricas"), por lo que no debe eliminarlas después de completar la instalación. De forma predeterminada, las secuencias de comandos se encuentran ubicadas en la carpeta en C:\\Archivos de programa\\Microsoft\\Microsoft WLAN-PEAP Tools.
  
**Para instalar las secuencias de comandos y las herramientas en cada servidor**
  
1.  Copie el archivo **PEAPWLAN.msi** proporcionado con la solución en el servidor.
  
2.  En el **Explorador de Windows**, haga doble clic en el archivo **PEAPWLAN.msi** y, a continuación, haga clic en **Siguiente** para iniciar la instalación.
  
3.  Si desea instalar las secuencias de comandos en una ubicación que no sea la predeterminada C:\\Archivos de programa\\Microsoft\\Microsoft WLAN-PEAP Tools, especifíquela.  
    Se le preguntará si desea instalar las secuencias de comandos para una sola cuenta o para todos los usuarios. Haga clic en **Todos los usuarios** y en **Siguiente** para continuar y, a continuación, vuelva a hacer clic en **Siguiente** de nuevo para confirmar.
  
4.  Tras completar la instalación, aparece el archivo **Tools Readme**. Este archivo contiene una renuncia importante y una breve descripción de las secuencias de comandos que se han instalado. Debe leerlo antes de continuar. Haga clic en **Siguiente** para continuar y, a continuación, haga clic en **Finalizar** para completar la instalación.
  
Para permitir un mejor acceso a estas secuencias de comandos, puede crear un acceso directo para abrir un shell de comandos en la carpeta donde se almacenan las secuencias de comandos.
  
**Para crear un acceso directo a MSS WLANS Tools**
  
1.  Desde el **Explorador de Windows** desplácese a la carpeta **MSS WLAN Tools**, cuya ubicación predeterminada es C:\\Archivos de programa\\Microsoft\\Microsoft WLAN-PEAP Tools.
  
2.  Haga doble clic en el archivo de secuencia de comandos por lotes **CreateShortcut.cmd**. Esto crea un acceso directo denominado MSS WLAN Tools en el escritorio.
  
3.  Puede que desee mover o copiar este acceso directo a su menú **Inicio**.
  
#### Utilización de las secuencias de comandos
  
Las secuencias de comandos se escriben en Windows Scripting Host utilizando lenguaje VBScript. Todas las secuencias de comandos funcionan de manera similar. Se deben ejecutar utilizando los dos archivos por lotes (MSSSetup.cmd y MSSTools.cmd) en lugar de ejecutarlos directamente. Los archivos por lotes simplifican la sintaxis de las secuencias de comandos.
  
La mayoría de las secuencias de comandos toman un solo parámetro que especifica la función que se va a realizar. Algunas secuencias de comandos toman parámetros adicionales (se explican en la guía). Las secuencias de comandos se ejecutan desde la carpeta en que se instalaron, es decir, desde un shell de comandos con el directorio de trabajo actual establecido en la carpeta de instalación de herramientas.
  
Las secuencias de comandos producen los siguientes tipos de resultados:
  
-   Cuadros de mensaje que muestran información o texto de alerta, solicitud de decisión o solicitud de entrada de datos.
  
-   Información de progreso detallada enviada a una ventana desplegable mientras la secuencia de comando se ejecuta. Si la secuencia de comandos encuentra un error, muestra información de error en la ventana. Cuando la ejecución de la secuencia de comandos se completa, se le solicita que cierre la ventana o que la deje abierta para una inspección posterior (por ejemplo, puede que desee mantener la ventana abierta para investigar errores).
  
-   Para muchas tareas, la información de progreso detallada también se escribe en un archivo de registro (%systemroot%\\debug\\ MSSWLAN-Setup.log). Su finalidad es la de utilizarlo en la resolución de problemas y la auditoría de instalación. Todas las tareas de instalación y configuración, así como la exportación e importación de la configuración de IAS se archivan en este registro. Por razones de seguridad, las tareas que crean los secretos de RADIUS (contraseñas) para los puntos de acceso inalámbrico no se registran.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de la infraestructura de directorio y de red
  
#### Configuración de la red
  
Debe conectar los componentes a la red como se muestra en la siguiente ilustración o según los requisitos específicos de su red.
  
[![](images/Dd162271.PEAP_301(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_301_big(es-es,technet.10).gif)
  
**Figura 3.1 Configuraciones simples de red WLAN**
  
Esta ilustración muestra la configuración más simple posible, donde los servidores IAS, los puntos de acceso y el resto de su red interna se conectan a la misma LAN. En instalaciones de mayor tamaño, la red está, normalmente, segmentada en varias LAN virtuales (VLAN) que se conectan mediante enrutadores o conmutadores de nivel 3. La configuración precisa cambiará considerablemente dependiendo de los requisitos individuales de la organización. La descripción detallada de este tema no entra en el ámbito de esta guía.
  
Para obtener más información sobre la configuración de la red para una infraestructura de WLAN, consulte el capítulo sobre la implementación de una LAN inalámbrica del *Kit de distribución de Windows Server 2003*.
  
##### Configuración de la red IP
  
La solución es, en gran parte, independiente de la distribución de la subred y la VLAN. Como se describe en el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas", puede elegir tener sus clientes inalámbricos en una VLAN diferente del resto de la red. Sin embargo, esta solución sólo se ha probado para el caso más simple, es decir, para un sitio determinado, los clientes inalámbricos se colocan en la misma LAN que el resto de la red y comparten la misma subred IP.
  
Si elige tener sus clientes inalámbricos en una VLAN independiente, debe asignar una subred IP independiente para los clientes inalámbricos y enlazar la VLAN inalámbrica al resto de su red mediante un enrutador o un conmutador de nivel 3. Para entornos más complejos, hay ventajas en configurar subredes independientes para sus clientes WLAN en cada sitio físico. Estas ventajas incluyen:
  
-   Puede mantener ámbitos de protocolo de configuración dinámica de host (DHCP) independientes para clientes con cable e inalámbricos; esto permite establecer un período de concesión mucho más corto para clientes WLAN.
  
-   Si tiene un entorno enrutado con varias subredes en el mismo sitio, la asignación de una sola subred para todos los clientes WLAN en ese sitio permite a esos clientes desplazarse por los puntos de acceso manteniendo la misma dirección IP.
  
-   Puede utilizar la subred de WLAN para definir un sitio de Active Directory y asociar la configuración de directiva de grupo con ese sitio. Sin embargo, no puede utilizar este mecanismo para aplicar la configuración de cliente WLAN del objeto de directiva de grupo descrita en el capítulo 6 "Configuración de clientes de LAN inalámbricas", ya que esta configuración necesita aplicarse a los clientes antes de que puedan conectarse correctamente a la WLAN.
  
#### DHCP
  
La información de direcciones IP y red IP necesita asignarse a los clientes WLAN. Esta solución utiliza el servicio DHCP de Windows para ello; así, debe haber un servicio DHCP para que lo utilicen los clientes WLAN.
  
Necesita asignar un ámbito DHCP independiente para cada subred donde implementará los clientes. Por ejemplo, si cuenta con dos sitios independientes con una conexión de red de área extensa (WAN) enrutada entre ellos, debe crear un ámbito DHCP para cada subred. Si va a asignar subredes independientes para sus clientes WLAN y LAN con cable, necesitará configurar un ámbito independiente para cada subred de WLAN. Además, si ha enrutado conexiones entre sus puntos de conexión y sus servidores DHCP, necesitará configurar agentes de retransmisión DHCP en los enrutadores o instalar el agente de retransmisión DHCP de Windows en un servidor de la misma subred que los puntos de acceso.
  
Para una mayor disponibilidad, deberá considerar la utilización de una configuración DHCP resistente con ámbitos divididos, DHCP agrupados o configuraciones DHCP en espera. Para obtener más información sobre este tema, consulte el capítulo sobre implementación de DHCP del *Kit de distribución de Windows Server 2003*.
  
#### DNS
  
Active Directory depende de un servicio de sistema de nombres de dominio (DNS) que debe funcionar correctamente. Esta solución se basa en el supuesto de que tal servicio está en vigor y operativo. Tendrá instalado DNS como parte del proceso de instalación de Active Directory o lo tendrá configurado por separado.
  
#### Active Directory
  
Esta solución se ha diseñado y probado utilizando la siguiente configuración de Active Directory:
  
-   Un bosque Active Directory de un solo dominio.
  
-   Los controladores de dominio de Windows Server 2003 (recién instalados, no los actualizados desde los controladores de dominio de Windows 2000).
  
-   Un nivel funcional de dominio del modo nativo de Windows 2000.
  
En muchos casos, es posible utilizar otras configuraciones de Active Directory, por ejemplo, mediante varios dominios o controladores de dominio de Windows 2000. En el texto se ofrece información adicional sobre la utilización de estas configuraciones, allí donde son compatibles con Microsoft. Sin embargo, estas configuraciones alternativas no forman parte de la solución principal probada.
  
##### Requisitos para todas las versiones de Active Directory
  
Un dominio en modo nativo permite crear grupos de seguridad universal de Active Directory. La utilización de grupos universales facilita la administración de directivas de acceso a redes de varios dominios. Sin embargo, para implementaciones de dominio único, esta configuración no tiene relevancia. Los comandos de instalación comprueban si el dominio está o no en modo nativo. Si el dominio está en modo nativo, la secuencia de comandos utilizará grupos universales pero, en caso contrario, sólo utilizará grupos globales.
  
Active Directory debe tener un esquema de Windows Server 2003. Es necesario para admitir la configuración de objetos de directiva de grupo de directivas de red inalámbrica. No hay necesidad de un nivel de funcionalidad de bosque Active Directory específico. En esta solución, se asume el nivel de funcionalidad de bosque de Windows 2000 predeterminado.
  
Para obtener más información sobre los conceptos de modo de dominio y bosque, consulte las referencias al final de este capítulo.
  
##### Utilización de los controladores de dominio de Windows 2000
  
En esta solución, IAS y los Servicios de Certificate Server se instalan en los sistemas de Windows Server 2003. No se ofrecen instrucciones para utilizar las versiones de Windows 2000 de estos componentes. Si está utilizando los controladores de dominio de Windows 2000 y no está pensando en actualizar ninguno a Windows Server 2003 debe actualizar el esquema al nivel de Windows 2003. Para obtener más información sobre la actualización del esquema, consulte la referencia al final de este capítulo.
  
Si esta solución se va a utilizar en un dominio o bosque utilizando controladores de dominio Windows 2000, debe asegurarse de que esos controladores de dominio tienen aplicado el Windows 2000 Service Pack 3 (SP3) o posterior. El Service Pack es necesario para asegurar que los controladores de dominio admiten firmas de protocolo ligero de acceso a directorios (LDAP). Ésta es una mejora de seguridad necesaria para los clientes de Windows XP y de entidad emisora de Windows Server 2003 que utilizan inscripción automática de certificados.
  
##### Comprobación de la seguridad de las directivas de cuenta de dominio
  
Esta solución se basa en contraseñas de usuario y equipo para autenticar usuarios y equipos para la WLAN. Por esta razón, es muy importante que no permita la utilización de contraseñas en blanco o poco seguras. Las contraseñas fácilmente predecibles facilitarán a un atacante la entrada a la WLAN. Ya que se utilizan las mismas contraseñas para autenticar al usuario o al equipo en el dominio, esto proporcionará también acceso al atacante a todos los recursos de red.
  
La forma más fácil de eliminar las contraseñas no seguras es establecer directivas de contraseñas seguras en el objeto de directiva de grupo de la directiva de dominio predeterminada. También debe aplicar una caducidad periódica para las contraseñas, una vigencia mínima de la contraseña y una comprobación del historial de la contraseña (para asegurarse de que los usuarios no utilizan de nuevo la misma).
  
**Advertencia:** debe advertir a los usuarios y administradores antes de cambiar la directiva de contraseña de dominio. Para evitar la frustración y la confusión entre los usuarios, es buena idea informarles inicialmente sobre la nueva directiva de contraseñas que planea adoptar, junto con instrucciones sobre la elección de contraseñas seguras.
  
Para ver las prácticas recomendadas para la directiva de contraseña de dominio, consulte la *Guía de seguridad de Windows Server 2003*. Al final de este capítulo se ofrece referencia para este documento.
  
##### Creación de grupos de seguridad
  
Utilice el procedimiento que se ofrece más adelante en esta sección para crear grupos de seguridad en Active Directory que utilizará con esta solución. Los grupos creados se enumeran en la tabla siguiente y, donde se indica, se muestran sus miembros. De forma predeterminada, estos grupos se crean en el contenedor de usuarios.
  
**Tabla 3.2. Miembros y grupos de seguridad**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Grupo de seguridad</th>
<th style="border:1px solid black;" >Finalidad</th>
<th style="border:1px solid black;" >Tipo de grupo</th>
<th style="border:1px solid black;" >Miembros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Usuarios de LAN inalámbrica</td>
<td style="border:1px solid black;">Especifica qué usuarios pueden autenticarse en la WLAN.</td>
<td style="border:1px solid black;">Global</td>
<td style="border:1px solid black;">Usuarios de dominio</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Equipos de LAN inalámbrica</td>
<td style="border:1px solid black;">Especifica qué equipos pueden autenticarse en la WLAN.</td>
<td style="border:1px solid black;">Global</td>
<td style="border:1px solid black;">Equipos de dominio</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Acceso a LAN inalámbrica</td>
<td style="border:1px solid black;">Este grupo se utiliza en la directiva de acceso de RADIUS para controlar el acceso a la WLAN.</td>
<td style="border:1px solid black;">Universal</td>
<td style="border:1px solid black;">Usuarios de LAN inalámbrica<br />
Equipos de LAN inalámbrica.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Configuración del equipo de LAN inalámbrica</td>
<td style="border:1px solid black;">Especifica qué equipos reciben configuración de WLAN de la directiva de grupo.</td>
<td style="border:1px solid black;">Dominio local</td>
<td style="border:1px solid black;">Equipos de LAN inalámbrica.</td>
</tr>
</tbody>
</table>
  
**Para crear y llenar los grupos de seguridad**
  
1.  Abra un shell de comandos con el acceso directo **MSS WLAN Tools**.
  
2.  En el símbolo del sistema, escriba *MSSSetup CreateWLANGroups* y, a continuación, presione **ENTRAR**.
  
    **Importante:** si ha movido los grupos de usuarios del dominio y de equipos del dominio de sus ubicaciones predeterminadas en el contenedor de usuarios, no se agregarán a los grupos de usuarios de LAN inalámbrica y equipos de LAN inalámbrica respectivamente. En ese caso, debe agregarlos a esos grupos de forma manual.
  
    **Nota:** si instala esta solución en un dominio de modo mixto, el grupo de acceso a la LAN inalámbrica se creará como un grupo global de dominio en lugar de un grupo universal. Esto indica que necesita crear uno de estos grupos en cada dominio si va a instalar esta solución en un bosque de varios dominios (esta tarea se describe en el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas").
  
    Si va a instalar esta solución en varios dominios, necesita crear los grupos globales de usuarios de LAN inalámbrica y equipos de LAN inalámbrica en cada dominio y agregarlos al grupo de acceso de LAN inalámbrica. También necesita crear un grupo local de dominio de configuración del equipo de LAN inalámbrica en cada dominio en el que tenga clientes WLAN y agregar el grupo universal de equipos de LAN inalámbrica como miembro.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Preparación de los servidores
  
Esta sección cubre la configuración específica de servidor. Necesita realizar la mayoría de los procedimientos siguientes para cada servidor que desee instalar como servidor IAS. El procedimiento de la sección sobre configuración de seguridad del servidor es la única excepción porque, aunque la configuración de seguridad se aplique a cada servidor, este procedimiento sólo se debe ejecutar una vez por dominio. La configuración se aplica automáticamente a otros servidores del dominio.
  
#### Sistemas operativos compatibles
  
Esta solución se ha creado y probado utilizando Windows Server 2003, Standard Edition para todos los componentes de servidor. Sin embargo, las secuencias de comandos de la instalación y la guía son las mismas para Windows Server 2003, Enterprise Edition.
  
Debería leer la sección "Uso de Windows Server Standard o Enterprise Edition" del capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas" antes de decidir si necesita utilizar Windows Server 2003, Enterprise Edition o no. La utilización de Windows Server 2003, Standard Edition limita la funcionalidad de los Servicios de Certificate Server y el número de puntos de acceso inalámbrico que puede admitir IAS que podrían (ambos o uno de los dos) no ser aceptados en grandes organizaciones.
  
Esta solución no se ha diseñado para admitir versiones anteriores de Windows Server y no se ha probado con ninguna de ellas. Estas versiones de Windows Server 2000 de IAS y Servicios de Certificate Server pueden funcionar para algunas o todas las funciones de servidor de esta solución, pero las instrucciones para ello quedan fuera del ámbito de esta documentación.
  
#### Directrices del hardware
  
El primer servidor que instale ejecutará los Servicios de Certificate Server así como IAS. Los Servicios de Certificate Server necesitan recursos mínimos en esta solución. Sin embargo, debería asegurar que la carga que IAS coloca en el servidor no afecta negativamente al rendimiento de sus funciones de controlador de dominio. Esto sólo suele ocurrir en las implementaciones de IAS más amplias. Si fuera necesario, debería agregar un controlador de dominio adicional al mismo sitio de Active Directory como compensación.
  
Si piensa activar el registro de RADIUS, deberá asignar un disco físico independiente para los registros.
  
**Tabla 3.3. Hardware mínimo recomendado para el servidor IAS**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Elemento</th>
<th style="border:1px solid black;" >Requisito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">CPU</td>
<td style="border:1px solid black;">Procesador a 733 MHz o superior</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Memoria</td>
<td style="border:1px solid black;">256 MB</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Interfaces de red</td>
<td style="border:1px solid black;">Adaptador único de red</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Almacenamiento en disco</td>
<td style="border:1px solid black;">Controladora RAID SCSI o IDE
2 x 18 GB (SCSI) o 2 x 20 GB (IDE) configurado como volumen RAID 1
Almacenamiento local de medios extraíbles (CD-RW o cinta para copia de seguridad), si no hay ningún servicio de copia de seguridad en red.
Unidad de disco de 1,44 MB para transferencia de datos.</td>
</tr>
</tbody>
</table>
 

Debería leer la sección "Requisitos del software y del hardware de IAS" del capítulo 2 "Planeamiento de la implementación de seguridad en LAN inalámbricas", para obtener más detalles sobre los requisitos de rendimiento de hardware.

#### Obtención e instalación de software compatible

Esta sección enumera el software adicional necesario en sus servidores. También describe cómo obtener e instalar el software.

##### Consola de administración de directivas de grupo

La consola de administración de directiva de grupo (GPMC) se utiliza para instalar y configurar los objetos de directiva de grupo utilizados por la solución. La GPMC sólo necesita instalarse en el primer servidor en el que se instala IAS, su instalación en servidores IAS posteriores es opcional.

**Nota:** la instalación de la GPMC cambia ligeramente la interfaz de usuario de los usuarios y equipos de Active Directory en el servidor en el que se ha instalado la GPMC. Para obtener más información sobre la utilización de la GPMC y descargas, consulte la referencia al final de este capítulo.

**Para instalar la consola de administración de directivas de grupo**

1.  Descargue el archivo de instalación **Gpmc.msi** del Centro de descargas de Microsoft.

2.  Asegúrese de que ha iniciado sesión como miembro del grupo de administradores de dominio (o el grupo de administradores locales del equipo en el que va a instalar la GPMC, si no lo va a instalar en un controlador de dominio).

3.  En el **Explorador de Windows** haga doble clic en el archivo de instalación **Gpmc.msi**.

4.  Siga las indicaciones del asistente para instalar la GPMC; acepte todas las opciones predeterminadas.

    **Importante:** debe instalar la GPMC en la carpeta de Archivos de programa (aunque no importa la unidad que esté activada). También debe utilizar la carpeta de instalación predeterminada —GPMC— de Archivos de programa (si cambia el nombre de la carpeta, debe actualizar el nombre de la carpeta utilizada para instalar la GPMC en el archivo Constants.txt). Los procedimientos posteriores utilizan algunas de las herramientas instaladas por la GPMC y si lo instala en cualquier otro lugar no podrán encontrar las herramientas de GPMC.

##### Herramientas de soporte técnico de Windows Server 2003

Los procedimientos y las secuencias de comandos de configuración de esta solución utilizan algunas de las herramientas de soporte técnico de Windows. Debe instalarlas desde el disco de instalación de Windows Server 2003. Las secuencias de comandos de configuración e instalación de entidades emisoras las necesitan, así que debe instalarlas en el servidor en el que se van a instalar los Servicios de Certificate Server. No son necesarias, sin embargo, en los otros servidores aunque puede que desee instalarlas.

**Para instalar las herramientas de soporte técnico de Windows Server 2003**

1.  Asegúrese de que ha iniciado sesión como miembro del grupo de administradores de dominio (o el grupo de administradores locales del equipo en el que está instalando las herramientas de soporte técnico, si no lo está instalando en un controlador de dominio).

2.  Inserte el **CD** de **instalación de Windows Server 2003** (o conéctese a la fuente de instalación si va a instalar desde la red o desde otros discos).

3.  Desde el **Explorador de Windows**, desplácese a la unidad de discos de instalación (unidad de CD o de disquete) y, a continuación, al archivo **\\support\\tools\\supptools.msi**. Haga doble clic en el archivo para empezar la instalación.

4.  Siga las indicaciones del asistente para instalar las herramientas de soporte y acepte el contrato de licencia y la carpeta de instalación predeterminada.

##### CAPICOM

CAPICOM es una interfaz convertible en secuencias de comandos en un conjunto de funciones de seguridad de Windows conocido como CryptoAPI (CAPI). CAPICOM es necesario para las secuencias de comandos de control de estado de los Servicios de Certificate Server y para crear los secretos de RADIUS utilizados para autenticar los puntos de acceso inalámbrico. Debe instalar la versión 2.0 o posterior de CAPICOM en todos los servidores IAS de su organización.

Puede encontrar la última versión de CAPICOM 2.0 en el Centro de descargas de Microsoft (consulte la sección "Referencias" al final de este capítulo).

El archivo de distribución de CAPICOM no contiene una instalación automática; por ello debe utilizar la secuencia de comandos por lotes InstCAPICOM.cmd (suministrada con esta solución). Si desea llevar a cabo estos pasos de forma manual, puede copiar los comandos de la secuencia de comandos por lotes.

**Para instalar CAPICOM**

1.  Descargue el archivo de distribución de **CAPICOM**, **CCR2INST.exe**, del Centro de descargas de Microsoft y cópielo en una carpeta temporal del servidor.

2.  Asegúrese de que ha iniciado sesión como miembro del grupo de administradores de dominio (o el grupo de administradores locales del equipo en el que está instalando CAPICOM, si no lo está instalando en un controlador de dominio).

3.  Abra un shell de comandos con el acceso directo **MSS WLAN Tools**.

4.  En el símbolo del sistema, escriba:

    *InstCAPICOM \[d:\]PathtoCCDistFile*\\CCR2INST.EXE y, a continuación, presione **ENTRAR**.

    **Nota:** sustituya *\[d:\]RutaArchivoDistribuciónCAPICOM* con la ruta completa (incluyendo la letra de la unidad, si es una distinta) de la carpeta en la que copió el archivo de distribución de CAPICOM.

##### Microsoft Baseline Security Analyzer (MBSA)

Esta herramienta es necesaria para comprobar que las actualizaciones de seguridad del sistema operativo son actuales y detectar posibles problemas con la configuración de seguridad de los servidores. Necesita utilizar la versión 1.1.1 o posterior de MBSA para explorar los sistemas de Windows Server 2003. Puede encontrar la última versión de MBSA en el Centro de descargas de Microsoft.

**Para instalar MBSA**

1.  Descargue el archivo de instalación **mbsasetup.msi** del Centro de descargas de Microsoft.

2.  Asegúrese de que ha iniciado sesión como miembro del grupo de administradores de dominio (o el grupo de administradores locales del equipo en el que está instalando MBSA, si no lo va a instalar en un controlador de dominio).

3.  En el **Explorador de Windows**, desplácese al archivo **mbsasetup.msi** y haga doble clic en él.

4.  Siga las indicaciones del asistente para instalar el MBSA; acepte todas las opciones predeterminadas.

#### Configuración de seguridad del servidor

En esta sección se describe cómo aplicar directivas de seguridad y otras medidas de seguridad a Windows Server 2003 antes de instalar IAS y Servicios de Certificate Server.

Esta solución está diseñada para instalarse en servidores existentes (normalmente controladores de dominio). La configuración de seguridad utilizada en esta sección es intencionadamente conservadora por el peligro que representa un conflicto entre la configuración de seguridad y los servicios y las aplicaciones instaladas que pueden estar ejecutándose en el servidor.

##### Utilización de la Guía de Seguridad de Windows Server 2003

Windows Server 2003 cuenta con una configuración de seguridad predeterminada segura. Para la mayoría de las organizaciones, esta configuración ofrece una buena protección para su sistema si se combina con un proceso de mantenimiento de actualizaciones efectivo (para obtener más detalles sobre el mantenimiento de actualizaciones, consulte la sección "Actualizaciones de seguridad del servidor" que aparece más adelante en este capítulo). Sin embargo, también debe tener en cuenta las recomendaciones descritas en la *Guía de seguridad de Windows Server 2003*. Esta guía define configuraciones de seguridad adecuadas para distintas funciones de servidor.

Los servidores utilizados en esta solución realizan varias funciones de servidor definidas en la *Guía de seguridad*; las funciones de controlador de dominio y de servidor de RADIUS para la mayoría de los servidores y, en el caso del servidor principal, también realiza la función de entidad emisora de certificados. Para cada función, la guía define una plantilla de seguridad con todas las configuraciones de seguridad adecuadas para esa función. Para un servidor con varias funciones, deberá aplicar una combinación de las plantillas de seguridad que correspondan a cada una de las funciones independientes del servidor. En sus servidores, también puede tener otros servicios de infraestructura como DNS, DHCP y el servicio de nombres de Internet de Windows (WINS), en cuyo caso necesita incluir las plantillas de seguridad adecuadas a estas funciones. Para obtener instrucciones sobre cómo llevarlo a cabo, consulte la *Guía de seguridad de Windows Server 2003*.

**Advertencia:** las plantillas de configuración de seguridad de la *Guía de seguridad de Windows Server 2003* desactivan específicamente un número de servicios que no son necesarios para las funciones de servidor definidas. Si dispone de cualquier otra aplicación o servicio en los servidores, debe probarlos para asegurarse de que las plantillas de seguridad no desactivan servicios ni cambian ninguna configuración de seguridad de la que dependen sus aplicaciones o servicios. Las instrucciones para combinar funciones y cambiar configuraciones para albergar otras aplicaciones también se incluyen en la *Guía de seguridad de Windows Server 2003*.

##### Aplicación de la configuración de seguridad

Al contrario que la mayoría de los otros procedimientos de la sección "Preparación de los servidores" de este capítulo, este procedimiento no necesita llevarse a cabo en cada servidor. En su lugar, las configuraciones se importan en un objeto de directiva de grupo de Active Directory y, a continuación, se aplican de forma global a todos los servidores.

Sólo hay dos tipos de configuraciones de seguridad aplicadas en esta solución. El primer tipo se aplica para configurar todos los servicios necesarios para iniciar automáticamente (en caso de que otra directiva de seguridad aplicada al equipo lo detenga o lo desactive). El segundo tipo se aplica para cambiar la directiva de auditoría de forma que los errores de auditoría para sucesos comunes (como inicio de sesión) también se guarden en el registro de seguridad.

La tabla siguiente muestra los servicios configurados para iniciarse automáticamente.

**Tabla 3.4. Servicios de Windows activados por directiva**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Servicio</th>
<th style="border:1px solid black;" >Configuración de directiva</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Servicios de Certificate Server</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servicio de autenticación de Internet</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Proveedor de instantáneas de software de Microsoft</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Almacenamiento de medios extraíbles</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Programador de tareas</td>
<td style="border:1px solid black;">Automático</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Instantáneas de volumen</td>
<td style="border:1px solid black;">Automático</td>
</tr>
</tbody>
</table>
  
La tabla siguiente muestra las categorías de auditoría donde se activa la auditoría de errores además de la auditoría de aciertos predeterminada.
  
**Tabla 3.5. Configuración de directiva de auditoría**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Directiva de auditoría</th>
<th style="border:1px solid black;" >Valor de configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Auditar sucesos de inicio de sesión de cuenta</td>
<td style="border:1px solid black;">Acierto/Error (sólo Acierto como valor predeterminado)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Auditar sucesos de administración de cuentas</td>
<td style="border:1px solid black;">Acierto/Error (sólo Acierto como valor predeterminado)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Auditar sucesos de inicio de sesión</td>
<td style="border:1px solid black;">Acierto/Error (sólo Acierto como valor predeterminado)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Auditar sucesos de cambio de directivas</td>
<td style="border:1px solid black;">Acierto/Error (sólo Acierto como valor predeterminado)</td>
</tr>
</tbody>
</table>
  
La habilitación de los valores de configuración de auditoría contemplados en la tabla aumentará los requisitos de almacenamiento para el registro de seguridad. Debe asegurarse de que se han establecido tamaños adecuados para los registros de sucesos en los controladores de dominio. El tamaño predeterminado para los registros de sucesos en Windows Server 2003 es más que adecuado, pero Windows 2000 utilizaba tamaños predeterminados que solían ser demasiado pequeños para un uso práctico (esta configuración puede ser aún efectiva si ha actualizado desde Windows 2000). En el capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas", comprobará cómo los servidores IAS están configurados para registrar todas las conexiones WLAN, sean correctas o erróneas, en el registro del sistema de Windows. Debe asegurarse de que se han establecido tamaños adecuados para los registros de seguridad y de sistema en los controladores de todos los dominios. Windows Server 2003 utiliza 16 MB para los registros del sistema y de la aplicación y 128 MB para los registros de seguridad: estos valores son adecuados para esta solución.
  
###### Importación del objeto de directiva de grupo de la configuración de seguridad
  
El siguiente procedimiento importa la configuración descrita en la sección anterior en el dominio, pero no la aplica a ningún servidor.
  
**Para instalar en su dominio el objeto de directiva de grupo de la configuración de seguridad**
  
1.  Abra un shell de comandos utilizando el acceso directo **MSS WLAN Tools**.
  
2.  En el símbolo del sistema, escriba el siguiente comando para importar en el dominio el objeto de directiva de grupo llamado Directivas de seguridad del servidor IAS:
  
    *MSSSetup ImportSecurityGPO,* y, a continuación, presione **ENTRAR**.
  
###### Aplicación de la configuración de seguridad en los controladores de todos los dominios
  
En este procedimiento, la configuración de seguridad se aplica a los controladores de todos los dominios (con o sin IAS instalado). No debería provocar ningún efecto adverso en las funciones de los controladores de dominio o en cualquier otra aplicación o servicio que se ejecute en ellos, puesto que el objeto de directiva de grupo no tiene ningún parámetro que deshabilite funcionalidades. Si no desea aplicar esta configuración a los controladores de su dominio, consulte el procedimiento que sigue inmediatamente a éste.
  
Para aplicar la configuración a los controladores de todos los dominios, necesita vincular el objeto de directiva de grupo importado a la unidad organizativa de controladores de dominio. El objeto de directiva de grupo se vincula manualmente debido al riesgo de sobrescribir los valores de este objeto ya configurados en su dominio.
  
**Para aplicar la configuración de seguridad en los controladores de todos los dominios**
  
1.  Para iniciar la **consola de administración de directiva de grupo**, haga clic en **Inicio**, **Todos** **los programas**, **Herramientas administrativas** y, a continuación, en **Administración de directiva de grupo**.
  
2.  Desplácese hasta la unidad organizativa de los **controladores de dominio** en el panel izquierdo y haga clic sobre ella.
  
    Esta unidad debe aparecer justo debajo del objeto dominio.
  
3.  Haga clic con el botón secundario en el nombre de la unidad organizativa y, a continuación, en **Vincular objeto de directiva de grupo existente**.
  
4.  En la lista de objetos, haga clic en **Directivas de seguridad del servidor IAS** y, a continuación, haga clic en **Aceptar** para volver a la ventana principal de la consola.
  
5.  En el panel derecho, asegúrese de que la ficha **Objetos de directiva de grupo vinculados** está seleccionada; a continuación, haga clic en el objeto de directiva de grupo **Directivas de seguridad del servidor IAS**.
  
6.  Haga clic en el símbolo con doble flecha hacia arriba que se encuentra justo a la izquierda de esta lista para mover este objeto a la prioridad más alta.
  
    Esto garantiza que los servicios requeridos permanecerán habilitados independientemente de otras directivas de seguridad aplicadas a los controladores de dominio.
  
7.  Cierre la **consola de administración de directiva de grupo**.
  
    La configuración de seguridad se aplicará a los servidores en el siguiente intervalo de actualización de objetos de directiva de grupo (el intervalo de actualización predeterminado es de cinco minutos para los controladores de dominio).
  
###### Aplicación de la configuración de seguridad sólo en los servidores IAS
  
Si no desea que la configuración de seguridad se aplique a los controladores de todos los dominios (o si ha optado por no instalar IAS en los controladores de dominio), puede crear una unidad organizativa aparte para los servidores IAS y, a continuación, aplicar a ésta el objeto de directiva de grupo. Si no está instalando IAS en los controladores de dominio, debe crear la unidad organizativa de los servidores IAS en alguna otra parte del dominio.
  
**Para aplicar la configuración de seguridad sólo a los servidores IAS**
  
1.  Para iniciar la **consola de administración de directiva de grupo**, haga clic en **Inicio**, **Todos** **los programas**, **Herramientas administrativas** y, a continuación, en **Administración de directiva de grupo**.
  
2.  Desplácese hasta la unidad organizativa de los **controladores de dominio** en el panel izquierdo y haga clic sobre ella.
  
    Esta unidad organizativa se encuentra justo debajo de la raíz del dominio.
  
3.  Cree una nueva unidad organizativa de nivel secundario debajo de esta unidad. Para ello, haga clic con el botón secundario en el nombre de la unidad organizativa de **controladores de dominio** y, a continuación, seleccione **Nueva unidad organizativa** del menú emergente.
  
4.  Escriba un nombre para la unidad cuando se le solicite, por ejemplo, *Servidores IAS*.
  
5.  Haga clic con el botón secundario en esta unidad organizativa y, a continuación, en **Vincular objeto de directiva de grupo existente**.
  
6.  En la lista de objetos, seleccione **Directivas de seguridad del servidor IAS** y, a continuación, haga clic en **Aceptar** para volver a la ventana principal de la consola.
  
7.  Cierre la **consola de administración de directiva de grupo**.
  
8.  Mueva el objeto equipo de cada controlador de dominio combinado y el servidor IAS desde la unidad organizativa de **controladores de dominio** hasta la nueva unidad organizativa de nivel secundario.
  
    La configuración de seguridad se aplicará a los servidores en el siguiente intervalo de actualización de objetos de directiva de grupo (el intervalo de actualización predeterminado es de 5 minutos para los controladores de dominio y de 90 minutos para otros equipos).
  
    **Nota:** si va a instalar servidores IAS en varios dominios, necesita volver a instalar y vincular los objetos de directiva de grupo para cada dominio del bosque.
  
###### Comprobación de la configuración de seguridad
  
**Para comprobar que se ha aplicado la configuración de seguridad**
  
1.  Desde un shell de comandos, en el símbolo de sistema, escriba:
  
    *gpupdate /force*y, a continuación, presione **ENTRAR**.
  
2.  En el registro de **sucesos de aplicación**, compruebe los sucesos de origen **SceCli** (puede tardar unos segundos en aparecer). Debe aparecer registrada una Id. de suceso 1704. El texto del suceso debe ser:
  
    Se ha aplicado satisfactoriamente la directiva de seguridad en los objetos de directiva de grupo.
  
#### Actualizaciones de seguridad del servidor
  
A diferencia de la configuración de seguridad del objeto de directiva de grupo, es necesario comprobar y aplicar las actualizaciones de seguridad en cada servidor. Si tiene que administrar pocos servidores, puede utilizar procedimientos manuales. Si tiene muchos servidores y aún no dispone de un sistema de mantenimiento actualizado automático, la comprobación y aplicación manuales de actualizaciones en todos los servidores puede ser una tarea extremadamente tediosa. En cambio, debe considerar automatizar la aplicación de actualizaciones de seguridad mediante Microsoft Software Update Service (SUS) o Microsoft Systems Management Server (SMS) 2003. Para obtener más información sobre su uso, consulte la *Microsoft Guide to Security Patch Management*.
  
##### Comprobación de actualizaciones de seguridad actuales
  
Existen dos formas de comprobar la versión de las actualizaciones de seguridad de su servidor, en concreto Windows Update y Microsoft Baseline Security Analyzer (MBSA). Existen también otras herramientas, que realizan funciones similares, facilitadas por proveedores distintos a Microsoft.
  
###### Windows Update
  
Windows Update es un servicio en línea diseñado principalmente para su uso por parte de pequeñas empresas y de usuarios en casa, aunque no existe ninguna restricción sobre los usuarios del servicio. Dado que Windows Update exige estar conectado a Internet, no debe utilizar este servicio sin proteger el servidor con un servidor de seguridad.
  
Para obtener más información sobre Windows Update, consulte las referencias al final de este capítulo.
  
###### Microsoft Baseline Security Analyzer
  
MBSA es una herramienta de evaluación de seguridad que comprueba la existencia de problemas de seguridad en el sistema, incluidas las actualizaciones que faltan. Para obtener más información sobre MBSA, consulte las referencias al final de este capítulo.
  
**Para comprobar las actualizaciones de seguridad instaladas con MBSA**
  
1.  Si su servidor no tiene conectividad con Internet, debe obtener cada vez la versión actual de la base de datos de seguridad de MBSA antes de ejecutar la comprobación. Se trata de un archivo XML, **msecure.xm.**, que se puede descargar de la URL facilitada al final de este capítulo. Copie este archivo a la carpeta en la que ha instalado MBSA (la carpeta predeterminada es C:\\Archivos de programa\\Microsoft Baseline Security Analyzer).
  
2.  Para comprobar el estado de actualización actual del servidor, escriba en el símbolo del sistema:
  
    *Mbsacli /hf -v* y, a continuación, presione **ENTRAR**.
  
3.  Anote las actualizaciones de seguridad que faltan. Éstas se muestran como sigue:
  
    \* WINDOWS SERVER 2003, STANDARD EDITION GOLD
  
    Nota MS03-030 819696
  
    Para obtener una explicación pormenorizada, consulte Q306460.
  
4.  Puede obtener la actualización de seguridad asociada a cada actualización de seguridad que le falte con la ayuda de su explorador Web, el cual le dará acceso al artículo de Microsoft Knowledge Base relacionado. Escriba la siguiente dirección URL en el explorador:
  
    *http://support.microsoft.com/default.aspx?kbid=XXXXXX*
  
    **Nota:** debe reemplazar XXXXXX con el número o números del artículo de Microsoft Knowledge Base enumerado(s) en los resultados de MBSA (por ejemplo, 819696 en el ejemplo anterior).
  
5.  Instale cada actualización según las instrucciones del artículo de Microsoft Knowledge Base.
  
##### Utilización de MBSA para comprobar otros problemas de seguridad
  
Además de para comprobar que las actualizaciones de seguridad sean las últimas, debe utilizar MBSA para comprobar en el servidor otros problemas potenciales de seguridad. Para ello, ejecute la versión gráfica (desde el menú **Inicio**), explore el servidor y actúe según las advertencias.
  
En concreto, debe prestar atención a las cuentas de usuario detectadas con contraseñas en blanco, inseguras o sin límite de validez. No obstante, no modifique la configuración de ninguna cuenta integrada como krbtgt.
  
A menos que cambie la configuración predeterminada de la zona de seguridad de Internet Explorer, puede hacer caso omiso a las advertencias de MBSA sobre configuraciones no estándar. La configuración predeterminada de Windows Server 2003 es más segura que la configuración de las zonas de Internet Explorer que está comprobando MBSA.
  
El procedimiento expuesto en este capítulo sólo cubre la ejecución de MBSA para explorar el equipo local. El procedimiento para ejecutarlo y explorar los equipos de la red está fuera del alcance de estas instrucciones. Para obtener más detalles sobre el uso de MBSA, consulte la referencia al final del capítulo.
  
##### Administración e instalación de actualizaciones en los servidores
  
La cobertura total de la administración de actualizaciones automáticas continuas está fuera del alcance de estas instrucciones. No obstante, debe ser consciente de las tres formas principales que existen para la administración continua de las actualizaciones del sistema mediante la tecnología Microsoft.
  
###### AutoUpdate
  
AutoUpdate es un servido integrado en los servidores y clientes Windows que permite que cada equipo compruebe y descargue toda revisión de seguridad importante conforme son publicadas por Microsoft. Dispone de la opción para que las actualizaciones se instalen de manera automática. Esto requiere que cada equipo tenga acceso al Web (HTTP). En esta ocasión, también debe tener la precaución de contar con la protección de un servidor de seguridad adecuado para cada dispositivo (consulte la sección "Windows Update").
  
Para obtener más información sobre AutoUpdate, consulte las referencias al final de este capítulo.
  
###### Software Update Service
  
Software Update Service (SUS) perfecciona el servicio de AutoUpdate. Elimina la necesidad de que cada equipo esté conectado a Internet mediante la centralización de la comprobación de actualizaciones y la descarga de la funcionalidad en un equipo central o en varios. El administrador puede entonces aprobar o rechazar las actualizaciones descargadas en el servidor o servidores SUS. Todos los equipos de la organización recuperan todas las actualizaciones aprobadas. Estos equipos utilizan el servicio AutoUpdate para comprobar y descargar las actualizaciones desde el servidor o servidores SUS, en lugar de hacerlo desde el sitio Web de Windows Update.
  
Para obtener instrucciones sobre cómo implementar SUS, consulte *Patch Management Using Microsoft Software Update Services*. La dirección URL del mismo se proporciona al final de este capítulo.
  
###### Administración de las actualizaciones con Microsoft Systems Management Server
  
Con Microsoft SMS 2003, puede automatizar completamente la distribución de los Service Pack, las actualizaciones de seguridad y las de software. SMS 2000 con el Software Update Services Feature Pack integra las características de SUS con las capacidades más amplias de SMS. Tanto SMS 2000 como SMS 2003 incluyen la capacidad de programar las exploraciones de MBSA de todos los equipos de la organización. Si desea obtener más información acerca del uso de SMS, consulte los siguientes documentos:
  
-   *Patch Management Using Microsoft Systems Management Server 2003*
  
-   *Patch Management Using Microsoft Systems Management Server 2.0*
  
Las direcciones URL de estos documentos se proporcionan al final del capítulo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Este capítulo ha ofrecido instrucciones sobre la preparación de la red, de Active Directory, de los controladores de dominio y de otros elementos del entorno para instalar una infraestructura de WLAN segura. Las secuencias de comandos utilizadas para configurar esta solución se instalaron junto con una serie de herramientas de soporte técnico. Los grupos de seguridad utilizados por la solución se crearon en el dominio y la configuración de seguridad se importó y aplicó a los servidores. Por último, la versión de las actualizaciones de seguridad en los servidores se examinó y se corrigió si procedía.
  
El capítulo siguiente versa sobre la instalación de los Servicios de Certificate Server en el servidor principal instalado para crear la entidad emisora de certificados de red.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Referencias
  
Esta sección ofrece referencias a otra información complementaria importante u otro material informativo de relevancia para el contenido de este capítulo.
  
-   El capítulo sobre las LAN inálámbricas del Kit de distribución de Microsoft Windows Server 2003 se puede consultar en la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/deployguide/DNSBM\_WIR\_OVERVIEW.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/deployguide/dnsbm_wir_overview.mspx)
  
-   Para obtener más información sobre los niveles funcionales de dominio en Active Directory y sobre las instrucciones acerca de cómo cambiar entre ellos, consulte las siguientes secciones de la documentación de Windows Server 2003 en las siguientes URL:
  
    -   Esta sección describe los distintos niveles de bosque y de dominio:
  
        [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
        proddocs/standard/sag\_levels.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/standard/sag_levels.mspx)
  
    -   Esta sección describe cómo cambiar los niveles de bosque y de dominio:
  
        [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
        proddocs/standard/sag\_changedomlevel.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/standard/sag_changedomlevel.mspx)
  
-   Para obtener información detallada sobre la actualización del esquema de Active Directory en Windows 2000 al nivel de Windows Server 2003, consulte la página del documento ADPrep en la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/standard/adprep.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/standard/adprep.mspx)
  
-   Para obtener más información sobre la descarga y utilización de la consola de administración de directivas de grupo, consulte la siguiente dirección URL:
  
    [http://go.microsoft.com/fwlink/?LinkID=8630](http://go.microsoft.com/fwlink/?linkid=8630)
  
-   Para descargar la versión 2.0.0.3 de CAPICOM, consulte la siguiente dirección URL:
  
    [http://www.microsoft.com/downloads/details.aspx?  
    displaylang=en&FamilyID=860EE43A-A843-462F-ABB5-FF88EA5896F6](http://www.microsoft.com/downloads/details.aspx?displaylang=en&familyid=860ee43a-a843-462f-abb5-ff88ea5896f6)
  
    No obstante, para asegurarse de que se trata de la última versión, busque "CAPICOM" en la siguiente dirección URL:
  
    <http://www.microsoft.com/downloads>
  
-   Para obtener instrucciones sobre la descarga y utilización de Microsoft Baseline Security Analyzer (MBSA), consulte la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/security/tools/mbsahome.mspx](http://technet.microsoft.com/es-es/security/cc184924.aspx)
  
-   Para descargar la base de datos más reciente de Microsoft Patch (mssecure.xml) en forma de archivo CAB firmado, consulte la siguiente dirección URL:
  
    [http://download.microsoft.com/download/xml/security/  
    1.0/nt5/en-us/mssecure.cab](http://technet.microsoft.com/en-us/library/cc180646.aspx)
  
-   La Guía de seguridad de Microsoft Windows Server 2003 está disponible en:
  
    [http://go.microsoft.com/fwlink/?LinkId=14845](http://go.microsoft.com/fwlink/?linkid=14845)
  
-   Para obtener más información sobre Windows Update, consulte la siguiente dirección URL:
  
    <http://v4.windowsupdate.microsoft.com/en/default.asp>
  
-   Para obtener más información sobre la utilización de AutoUpdate, consulte el artículo en la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/standard/autoupdate\_top.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/standard/autoupdate_top.mspx)
  
-   Consulte la administración de revisiones, actualizaciones de seguridad y páginas de descarga en la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/security/topics/patch/default.mspx](http://technet.microsoft.com/es-es/security/bb977553.aspx)
  
-   La URL anterior ofrece vínculos a las siguientes guías y a otras relevantes:
  
    -   Patch Management Using Microsoft Software Update Services
  
    -   Patch Management Using Microsoft Systems Management Server 2003
  
    -   Patch Management Using Microsoft Systems Management Server 2.0
  
(Este artículo contiene referencias a guías de otros productos y vínculos a sitios Web que sólo están disponibles en inglés.)
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 4: Creación de la entidad emisora de certificados de red
  
[](#eiaaa)[Información general](#eiaaa)  
[](#ehaaa)[Requisitos previos del capítulo](#ehaaa)  
[](#egaaa)[Preparación de la implementación](#egaaa)  
[](#efaaa)[Comprobación de la preparación para la instalación](#efaaa)  
[](#eeaaa)[Instalación de Servicios de Certificate Server](#eeaaa)  
[](#edaaa)[Configuración de la entidad emisora](#edaaa)  
[](#ecaaa)[Resumen](#ecaaa)  
[](#ebaaa)[Referencias](#ebaaa)
  
### Información general
  
Este capítulo sirve de guía para instalar y configurar Servicios de Certificate Server Microsoft® Windows Server™ 2003. Servicios de Certificate Server es un componente opcional de Windows Server 2003 que no se instala de forma predeterminada.
  
Una instalación de Servicios de Certificate Server se conoce como una Entidad emisora de certificados. Sólo se necesita una entidad emisora de certificados para la solución *Seguridad en LAN inalámbricas con PEAP y contraseñas*. Esta entidad emisora se utilizará para emitir certificados en los servidores IAS (Servicio de autenticación de Internet), tal como se describe en los siguientes capítulos de esta solución.
  
El objetivo de este capítulo es proporcionar una entidad emisora específica muy sencilla. A diferencia de la mayoría de las entidades emisoras, se utilizará para emitir sólo un tipo de certificado: certificados de servidor para los servidores IAS que se utilizan en esta solución. Por este motivo, se ha diseñado para que se sea especialmente fácil de instalar, configurar y administrar. Es importante tener en cuenta que si la organización tiene previsto utilizar certificados para otros objetivos en el futuro, por ejemplo, IPSec o VPN, Microsoft recomienda una arquitectura de Infraestructura de claves públicas más sólida para el entorno. Consulte los materiales de planeamiento que se describen en el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas", para obtener más información.
  
La información que se incluye en este capítulo se limita a las instrucciones de implementación de la entidad emisora de certificados. En este capítulo no se explica ningún concepto general de infraestructura de claves públicas ni ninguno de los detalles de implementación de Servicios de Certificate Server de Microsoft aparte de los necesarios para completar la instalación. Tampoco se analiza el uso de esta entidad emisora para emitir otro tipo de certificados que no sean los certificados de autenticación de servidores IAS.
  
Este capítulo se basa en el supuesto de que actualmente no tiene una infraestructura de claves públicas en la organización. Si tiene una, podrá emitir certificados en los servidores IAS desde ella, en lugar de instalar la entidad emisora que se describe en este capítulo. No obstante, no entra en los objetivos de esta solución proporcionar información sobre cómo emitir los certificados desde la infraestructura de claves públicas o sobre cómo instalar esta entidad emisora en una infraestructura de claves públicas existente.
  
En lugar de instalar su propia entidad emisora, puede obtener certificados de una entidad emisora de certificados comercial como, por ejemplo, VeriSign o Thawte. Si desea ver un análisis sobre las ventajas relativas que ofrece instalar su propia entidad emisora frente a comprar certificados de un proveedor externo, consulte la sección "Obtención de certificados para servidores IAS" en el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas". Este capítulo no incluye información sobre la obtención y el uso de certificados de una entidad emisora de certificados comercial. No obstante, al final del capítulo se hace referencia a un documento de Microsoft donde se describe este proceso.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Requisitos previos del capítulo
  
Además de los requisitos previos que se describen en el capítulo 3, "Preparación del entorno", debe estar familiarizado con los conceptos de Servicios de Certificate Server y de infraestructura de claves públicas (aunque no se necesita un conocimiento especializado).
  
Antes de implementar las instrucciones de este capítulo, debe leer e implementar las instrucciones proporcionadas en el capítulo 3, "Preparación del entorno". Asimismo, se recomienda leer también la información sobre el diseño y el planeamiento del capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas" y tener un buen conocimiento de la arquitectura y el diseño de la solución.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Preparación de la implementación
  
#### Permisos necesarios
  
Para llevar a cabo los procedimientos de este capítulo, debe iniciar sesión con una cuenta que pertenezca a los siguientes grupos:
  
-   El grupo **Admins. del dominio** para el dominio en el que se va a instalar la entidad emisora.
  
-   El grupo **Administradores de organización** del bosque de servicio de directorios de Microsoft Active Directory®.
  
De forma predeterminada, la cuenta de administrador integrada del dominio raíz del bosque (el primer dominio creado en el bosque) pertenece a ambos grupos, aunque puede utilizar cualquier otra cuenta que pertenezca a esos grupos.
  
**Nota:** si no instala la entidad emisora de certificados en el dominio raíz del bosque y el bosque es Windows 2000 Active Directory (o se ha actualizado desde Windows 2000 Active Directory), la cuenta utilizada para la instalación también tendrá que ser miembro del dominio raíz del bosque.
  
#### Herramientas necesarias
  
Necesita las siguientes herramientas para llevar a cabo los procedimientos de este capítulo.
  
**Tabla 4.1. Herramientas necesarias para crear e instalar una entidad emisora de certificados**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Herramienta</th>
<th style="border:1px solid black;" >Descripción</th>
<th style="border:1px solid black;" >Fuente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Herramientas de seguridad en WLAN de MSS</td>
<td style="border:1px solid black;">Conjunto de secuencias de comandos y herramientas que se incluyen en esta solución.</td>
<td style="border:1px solid black;">Los pasos de instalación se incluyen en el capítulo 3.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Consola de administración de directivas de grupo</td>
<td style="border:1px solid black;">Herramienta de administración avanzada para importar y exportar grupos de directiva de grupo.</td>
<td style="border:1px solid black;">Los pasos de instalación se incluyen en el capítulo 3.<br />
Se puede descargar de Microsoft.com.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">CAPICOM</td>
<td style="border:1px solid black;">Biblioteca del sistema que permite ejecutar secuencias de comandos de operaciones de certificado y seguridad.</td>
<td style="border:1px solid black;">Los pasos de instalación se incluyen en el capítulo 3.<br />
Se puede descargar de Microsoft.com.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">DSACLs.exe</td>
<td style="border:1px solid black;">Herramienta de línea de comandos, que permite establecer permisos en los objetos de Active Directory.</td>
<td style="border:1px solid black;">Los pasos de instalación se incluyen en el capítulo 3.<br />
Disponible como parte del CD de instalación de Windows Server 2003.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Usuarios y equipos de Active Directory</td>
<td style="border:1px solid black;">Herramienta de Microsoft Management Console (MMC) utilizada para administrar usuarios, grupos, equipos y otros objetos de Active Directory.</td>
<td style="border:1px solid black;">Instalado como parte de Windows Server 2003.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Herramienta administrativa de entidad emisora de certificados.</td>
<td style="border:1px solid black;">Una herramienta de MMC que se utiliza para administrar la entidad emisora.</td>
<td style="border:1px solid black;">Se instala como parte de la instalación de Servicios de Certificate Server en Windows Server 2003.</td>
</tr>
</tbody>
</table>
  
#### Parámetros de la entidad emisora de certificados
  
En la siguiente tabla se muestran los parámetros utilizados en la instalación y configuración de la entidad emisora en esta solución. Todos estos parámetros se definen en el archivo de secuencia de comandos PKIparams.vbs y se pueden modificar en él cuando sea necesario.
  
**Tabla 4.2. Configuración de la entidad emisora de certificados utilizada en la solución**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetros de configuración de la entidad emisora</th>
<th style="border:1px solid black;" >Valor de configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Unidad y ruta de acceso de los archivos de solicitud de Servicios de Certificate Server</td>
<td style="border:1px solid black;">C:\CAConfig</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Longitud de clave de la entidad emisora</td>
<td style="border:1px solid black;">2048 bits</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Período de validez del certificado de la entidad emisora</td>
<td style="border:1px solid black;">25 años</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Período máximo de validez de los certificados emitidos por la entidad emisora</td>
<td style="border:1px solid black;">2 años</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Intervalo de publicación de lista de revocación de certificados para la entidad emisora de certificados</td>
<td style="border:1px solid black;">7 días</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Período de coincidencia de la lista de revocación de certificados (es decir, el tiempo transcurrido entre la publicación de una nueva lista de revocación de certificados y la fecha de caducidad de una lista de revocación de certificados antigua)</td>
<td style="border:1px solid black;">4 días</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Publicación de diferencias entre listas de revocación de certificados desactivada</td>
<td style="border:1px solid black;">0</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Plantillas de certificado disponibles en la entidad emisora</td>
<td style="border:1px solid black;">Equipo (máquina)</td>
</tr>
</tbody>
</table>
  
**Nota:** el período de validez de la entidad emisora de certificados se define con un valor grande para evitar la carga administrativa adicional que supone tener que renovar el certificado de la entidad emisora periódicamente. A diferencia de los certificados emitidos en equipos y usuarios, los certificados de la entidad emisora no se pueden renovar automáticamente y si no se renuevan antes de caducar, todos los certificados emitidos por la entidad emisora fallarán.
  
**Importante:** la configuración incluida en la tabla anterior se utilizó en las pruebas internas de esta solución y su funcionamiento está garantizado tal y como se describe. Muchos de estos valores se pueden modificar, pero sólo debería hacerlo si comprende perfectamente la finalidad de un valor de configuración concreto y lo que implicaría su modificación.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Comprobación de la preparación para la instalación
  
Antes de instalar los Servicios de Certificate Server en el servidor, asegúrese de que se pueda conectar con el dominio y que se hayan instalado las herramientas necesarias.
  
**Para comprobar el servidor antes de instalar la entidad emisora de certificados**
  
1.  Inicie una sesión en el servidor donde desee instalar la entidad emisora de certificados y la primera instancia del servidor IAS (utilizando una cuenta con los permisos administrativos adecuados).
  
2.  Haga clic en el acceso directo **MSS WLAN Tools** para abrir el shell de comandos y, en el símbolo del sistema, escriba:
  
    *MSSsetup CheckCAenvironment*
  
    El nombre del dominio en el que se instala la entidad emisora de certificados aparece en formato de nombre distintivo (DN) (por ejemplo, dc=Treyresearch, dc=net), que es equivalente a un formato de sistema de nombres de dominio (DNS) (Treyresearch.net).
  
3.  Si el nombre del dominio es correcto, haga clic en **Aceptar**. Si es incorrecto, haga clic en **Cancelar**, inicie una sesión en el dominio correcto y repita los pasos 1 y 2.
  
La secuencia de comandos comprueba que:
  
-   Se puede conectar con el controlador de dominio de Active Directory.
  
-   CAPICOM está instalado.
  
-   GPMC está instalado.
  
-   DSACLs.exe está instalado y se puede tener acceso a él.
  
Si se detecta algún problema, se le notifica con un error registrado en la ventana de la consola de la secuencia de comandos. Debe investigar y corregir este error antes de continuar.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Instalación de Servicios de Certificate Server
  
En esta sección se describe la instalación de Servicios de Certificate Server para crear una entidad emisora de certificados. La entidad emisora de certificados se instala como una entidad emisora raíz de empresa.
  
#### Instalación de componentes de software de Servicios de Certificate Server
  
Debe instalar los componentes de software de la entidad emisora de certificados mediante la secuencia de comandos proporcionada. Esta secuencia de comandos utiliza el administrador de instalación de componentes opcionales de Windows para instalar la entidad emisora de certificados y crea todos los archivos de configuración necesarios a medida que se ejecuta. Para realizar la instalación, utilice el CD de instalación de Windows Server 2003 (o la ruta de red del origen de instalación de Windows).
  
**Precaución:** si se ha instalado una entidad emisora de certificados anteriormente, o si intenta reinstalar la entidad emisora, debe eliminar primero la instalación existente. Antes de eliminar la entidad emisora, asegúrese de que no la esté utilizando ninguna otra aplicación.
  
Utilice **Agregar o quitar componentes de Windows** del subprograma **Agregar o quitar programas** en el **Panel de control** para eliminar los Servicios de Certificate Server.
  
**Para instalar Servicios de Certificate Server**
  
1.  Utilice el acceso directo **MSS WLANTools** para abrir un shell de comandos.
  
2.  En el símbolo del sistema, escriba lo siguiente para instalar los componentes de software de Servicios de Certificate Server:
  
    *MSSsetup InstallCA* y, a continuación, presione **ENTRAR**.
  
3.  Cuando se le indique, escriba un nombre para la entidad emisora de certificados.
  
    El nombre debe ser descriptivo y exclusivo en la organización (por ejemplo, entidad emisora de certificados de red de investigación de Trey).
  
4.  Para confirmar el nombre, haga clic en **Aceptar**.
  
    Para editar el nombre, haga clic en **No**.
  
    Para detener la instalación, haga clic en **Cancelar**.
  
    La secuencia de comandos creará los archivos de parámetros de instalación. Cuando finalice esta operación, se le solicitará que continúe con la instalación.
  
5.  Haga clic en **Aceptar** para continuar o haga clic en **Cancelar** para detener la instalación.
  
    **Nota:** si cancela aquí la instalación, el archivo de configuración — CAPolicy.inf — y el archivo de parámetros de componentes opcionales — OC\_CertSrv.txt — se dejarán en la carpeta Windows y en la carpeta de trabajo actual, respectivamente. Puede modificar estos archivos y utilizarlos en la instalación personalizada si no desea aceptar los valores predeterminados de la solución.
  
6.  Cuando aparezca el mensaje de confirmación indicándole que la instalación ha finalizado, haga clic en **Aceptar**.
  
#### Comprobación de la instalación de la entidad emisora de certificados
  
Puede comprobar que la instalación de los Servicios de Certificate Server ha sido correcta mediante el siguiente procedimiento.
  
**Para comprobar que la instalación de la entidad emisora de certificados es correcta**
  
1.  Utilice el acceso directo **MSS WLAN Tools** para abrir el shell de comandos.
  
2.  En el símbolo del sistema, escriba:
  
    *MSSsetup VerifyCAInstall* y, a continuación, presione **ENTRAR**.
  
    El visor de certificados muestra el certificado de la entidad emisora.
  
3.  Haga clic en la ficha **General** del certificado y compruebe que los valores coinciden con los de la siguiente tabla.
  
    **Tabla 4.3. Propiedades de certificados de la entidad emisora**

 
    <table style="border:1px solid black;">
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >Atributo del certificado</th>
    <th style="border:1px solid black;" >Valor de configuración requerido</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">Emitido para</td>
    <td style="border:1px solid black;">El nombre de la entidad emisora que se ha introducido durante la instalación.</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">Emitido por</td>
    <td style="border:1px solid black;">El nombre de la entidad emisora que se ha introducido durante la instalación.</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">Válido de...a...</td>
    <td style="border:1px solid black;">El intervalo que se especifica aquí debe ser de 25 años.</td>
    </tr>
    </tbody>
    </table>
  
4.  Haga clic en la ficha **Ruta de certificación** y compruebe que sólo aparece un certificado en el campo de ruta de certificación. El estado del certificado debe mostrar **El certificado es correcto**.
  
5.  Haga clic en **Aceptar** para cerrar el visor de certificados.
  
Si alguno de los valores anteriores no es el que esperaba, debe volver a iniciar la instalación de los Servicios de Certificate Server.
  
**Nota:** si tiene que volver a ejecutar la instalación de la entidad emisora de certificados, debe eliminar primero los Servicios de Certificate Server instalados tal como se ha descrito anteriormente.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de la entidad emisora
  
Una vez instalada la entidad emisora de certificados, debe ejecutar algunas secuencias de comandos adicionales para configurar los parámetros de la entidad emisora que quedan.
  
#### Configuración de las propiedades de la entidad emisora
  
Este procedimiento establece un número de parámetros en la entidad emisora de certificados que controlan su comportamiento. Algunos de estos parámetros se establecen durante la instalación de la entidad emisora, mientras que otros se deben establecer después de la instalación. Los valores de dichos parámetros se especifican en la sección "Parámetros de la entidad emisora de certificados" que aparece anteriormente en este capítulo. La secuencia de comandos utilizada en este procedimiento configura las propiedades de la entidad emisora, como se describe en la siguiente tabla.
  
**Tabla 4.4. Propiedades de configuración de la entidad emisora de certificados**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Propiedad de la entidad emisora</th>
<th style="border:1px solid black;" >Descripción del valor de configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Direcciones URL de punto de distribución de la lista de revocación de certificados (CDP)</td>
<td style="border:1px solid black;">Especifica las ubicaciones desde las que se puede obtener una lista de revocación de certificados actual. En esta solución sólo se utiliza una dirección URL de Protocolo ligero de acceso a directorios (LDAP). Contiene la ruta de acceso LDAP de la lista de revocación de certificados publicada en Active Directory.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Direcciones URL de Acceso a la información de entidad emisora (AIA)</td>
<td style="border:1px solid black;">Indica la ubicación desde la que se puede obtener un certificado de la entidad emisora. Como ocurre con el CDP, sólo se utiliza la dirección URL de LDAP que apunta a Active Directory.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Período de validez</td>
<td style="border:1px solid black;">Indica el período de validez máximo de los certificados emitidos (no es el mismo que el período de validez del certificado de entidad emisora, que se establece durante la instalación).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Período de la lista de revocación de certificados</td>
<td style="border:1px solid black;">Indica la frecuencia de publicación de la lista de revocación de certificados.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Período de coincidencia de la lista de revocación de certificados</td>
<td style="border:1px solid black;">Indica el período de coincidencia entre la emisión de una nueva lista de revocación de certificados y la caducidad de la lista de revocación de certificados anterior.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Período de diferencia entre listas de revocación de certificados</td>
<td style="border:1px solid black;">Indica la frecuencia de publicación de diferencias entre listas de revocación de certificados. (En esta entidad emisora de certificados, la diferencia entre listas de revocación de certificados está deshabilitada.)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Auditoría de la entidad emisora</td>
<td style="border:1px solid black;">Indica la configuración de auditoría de la entidad emisora de certificados. (Toda la auditoría está habilitada de manera predeterminada.)</td>
</tr>
</tbody>
</table>
  
**Nota:** muchos de estos parámetros afectan a la configuración de la lista de revocación de certificados de la entidad emisora de certificados. Una lista de revocación de certificados es una lista de certificados que ha emitido la entidad emisora pero que el administrador ha cancelado (o revocado) posteriormente. Aunque probablemente no necesitará revocar ningún certificado durante la administración de esta solución, muchas aplicaciones se basan en la capacidad de leer una lista de revocación de certificados actual para comprobar el estado de revocación de un certificado (aunque la lista de revocación de certificados esté vacía). Si la aplicación no puede encontrar una lista de revocación de certificados, puede rechazar el certificado.
  
**Para configurar las propiedades de la entidad emisora de certificados**
  
1.  Utilice el acceso directo **MSS WLAN Tools** para abrir el shell de comandos.
  
2.  En el símbolo del sistema, escriba lo siguiente para configurar los componentes de la entidad emisora:
  
    *MSSsetup ConfigureCA* y, a continuación, presione **ENTRAR**.
  
    Durante la configuración, la secuencia de comandos se detiene durante 20 segundos para esperar a que termine una tarea en la entidad emisora de certificados. No es necesario responder los mensajes emergentes que anuncian este retraso.
  
3.  Haga clic en **Aceptar** para descartar este mensaje.
  
Si la secuencia de comandos informa de un error, investigue el motivo mediante un seguimiento del archivo de registro (%systemroot%\\debug\\MSSWLAN-Setup.log) y vuelva a ejecutar la secuencia de comandos después de corregir el problema.
  
**Nota:** puede volver a ejecutar esta secuencia de comandos de configuración las veces que sea necesario.
  
#### Importación del objeto de directiva de grupo de la solicitud de certificados automática
  
Este procedimiento importa el objeto de directiva de grupo de la directiva de inscripción automática de certificados IAS preconfigurado para permitir la emisión automática de certificados en los servidores IAS del dominio. Utiliza el servicio de solicitud de certificados automática (ACRS).
  
El ACRS no se debe confundir con las posibilidades de inscripción automática de Windows Server 2003, Enterprise Edition, aunque ambos realizan funciones parecidas. Es un servicio más limitado que la inscripción automática y ya se utilizó antes en Windows 2000. Sólo permite inscribir certificados de *equipo* (no de usuario) y sólo funciona con las plantillas de certificado de la versión 1. No obstante, el ACRS es adecuado para el uso limitado de certificados de esta solución y permite instalar la entidad emisora en la Standard Edition de Windows Server 2003 (más económica).
  
**Importante:** si hay varios dominios en el bosque de Active Directory, deberá repetir este procedimiento para cada dominio en el que instale un servidor IAS.
  
La secuencia de comandos que se utiliza en el siguiente procedimiento importa un objeto de directiva de grupo preconfigurado con una directiva para inscribir automáticamente los certificados. El objeto de directiva de grupo especifica el tipo de certificado "Equipo" predefinido como el tipo de la inscripción. A continuación, la secuencia de comandos aplica permisos de seguridad al objeto de directiva de grupo para que sólo afecte a los miembros del grupo de servidores IAS y RAS (el valor de configuración predeterminado es aplicar el objeto de directiva de grupo a todos los usuarios y equipos autenticados).
  
**Nota:** en algunos contextos, la plantilla de certificado Equipo se denomina plantilla Máquina. "Máquina" es el nombre interno de la plantilla, mientras que "Equipo" es el nombre de visualización.
  
**Para instalar en su dominio el objeto de directiva de grupo de la solicitud de certificados automática**
  
1.  Utilice el acceso directo **MSS WLAN Tools** para abrir el shell de comandos.
  
2.  En el símbolo del sistema, escriba lo siguiente para importar en el dominio el objeto de directiva de grupo de la directiva de inscripción automática de certificados IAS:
  
    *MSSsetup ImportAutoenrollGPO* y, a continuación, presione **ENTRAR**.
  
A continuación, vincule este objeto de directiva de grupo con el dominio para que se aplique la configuración del objeto de directiva de grupo a los servidores IAS. Éste es el procedimiento manual que permite controlar el proceso de vinculación del objeto de directiva de grupo. La automatización de este paso supone el riesgo de sobrescribir la configuración de vínculos del objeto de directiva de grupo existente del dominio.
  
**Para aplicar el objeto de directiva de grupo de la solicitud de certificados automática**
  
1.  Haga clic en **Inicio**, **Todos los programas**, **Herramientas administrativas** y, a continuación, en **Administración de directiva de grupo** para iniciar la **GPMC**.
  
2.  En el panel izquierdo de la **GPMC**, desplácese hasta el objeto de dominio correspondiente a su dominio.
  
    El objeto de dominio se encuentra en el contenedor de **Dominios** de nivel superior y tiene el mismo nombre que el nombre DNS del dominio.
  
3.  Haga clic con el botón secundario en el objeto de domino y, a continuación, seleccione **Vincular objeto de directiva de grupo existente**.
  
4.  En la lista de objetos de directiva de grupo, seleccione **Directiva de inscripción automática de certificados IAS**.
  
5.  Haga clic en **Aceptar** para volver a ejecutar la ventana principal de la **GPMC**.
  
6.  En el panel derecho, haga clic en la ficha **Objetos de directiva de grupo vinculados** y, a continuación, seleccione **Directiva de inscripción automática de certificados IAS**.
  
7.  Cierre la **GPMC**.
  
    La configuración de la solicitud de certificados automática se aplicará a los servidores sólo si han sido agregado como miembros del grupo de servidores IAS y RAS. Este asunto se tratará en un procedimiento del siguiente capítulo.
  
    **Importante:** si el dominio está en modo mixto y está instalando IAS en los servidores miembros (en lugar de en los controladores de dominio), el grupo local de servidores IAS y RAS no estará visible en los servidores miembros. Esto impide que el objeto de directiva de grupo de ACRS se aplique a estos servidores y detenga la inscripción de certificados de estos servidores. Para evitarlo, cree un grupo global de dominio, agregue a este grupo las cuentas de servidores miembros IAS y agregue el grupo a la lista de control de acceso (ACL) del objeto de directiva de grupo, otorgándole los permisos de **Aplicación** y **Lectura**.
  
#### Comprobación de la configuración de la entidad emisora
  
El siguiente procedimiento confirma que ha configurado correctamente la entidad emisora de certificados. La secuencia de comandos comprueba que:
  
-   La entidad emisora de certificados tiene el período de validez correcto (para los certificados emitidos).
  
-   El período de publicación de la lista de revocación de certificados es el correcto.
  
-   La entidad emisora de certificados tiene la plantilla de certificado Equipo asignada.
  
-   El objeto de directiva de grupo de la solicitud de certificados automática (inscripción automática) se ha importado correctamente al dominio.
  
Estos valores se comparan con la configuración almacenada en el archivo PKIParams.vbs. La secuencia de comandos no comprueba valores absolutos; sólo comprueba si la configuración se ha establecido correctamente en la entidad emisora de certificados.
  
**Para comprobar la configuración de la entidad emisora de certificados**
  
1.  Utilice el acceso directo **MSS WLAN Tools** para abrir el shell de comandos.
  
2.  En el símbolo del sistema, escriba lo siguiente para configurar los componentes de la entidad emisora:
  
    *MSSsetup VerifyCAConfig* y, a continuación, presione **ENTRAR**.
  
Si la salida de la secuencia de comandos muestra errores, debe revisar los pasos de este capítulo y rectificar los problemas indicados.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Este capítulo sirve de guía en el proceso de instalación de una entidad emisora de propósito específico para emitir certificados de servidor en servidores IAS. La configuración de la entidad emisora utilizada está diseñada para necesitar muy poco mantenimiento, por lo que necesitará una administración mínima en el futuro. No obstante, la información operativa y de soporte que necesite se incluye en el capítulo 8, "Mantenimiento de soluciones de seguridad en LAN inalámbricas".
  
Está listo para instalar los servidores IAS. Esto se describe en el capítulo 5, "Creación de la infraestructura de seguridad en LAN inalámbricas".
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Referencias
  
Esta sección ofrece referencias a otra información complementaria importante u otro material informativo de relevancia para el contenido de este capítulo.
  
-   Si desea una introducción a los conceptos de la infraestructura de claves públicas y las características de Servicios de Certificate Server de Windows 2000, consulte el documento "An Introduction to the Windows 2000 Public-Key Infrastructure" que hay disponible en la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/prodtechnol/windows2000serv/  
    evaluate/featfunc/pkiintro.mspx](http://technet.microsoft.com/en-us/library/cc768063.aspx)
  
-   Si desea una introducción a los conceptos de la infraestructura de claves públicas y las características de Servicios de Certificate Server de Windows 2000, consulte el documento "An Introduction to the Windows 2000 Public-Key Infrastructure" que hay disponible en la siguiente dirección URL:
  
    [http://www.microsoft.com/windowsxp/pro/techinfo/planning/  
    pkiwinxp/default.asp](http://www.microsoft.com/windowsxp/pro/techinfo/planning/pkiwinxp/default.asp)
  
-   Para obtener la documentación del producto que describe los conceptos clave y las tareas de administración, consulte la sección "Servicios de Certificate Server" en la documentación del producto Windows Server 2003 que hay disponible en la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/standard/SE\_PKI.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/standard/se_pki.mspx)
  
-   Para obtener información sobre cómo obtener y utilizar los certificados de una entidad emisora comercial, consulte el artículo "Obtaining and Installing a VeriSign WLAN Server Certificate for PEAP-MS-CHAP v2 Wireless Authentication", que hay disponible en la siguiente dirección URL:
  
    [http://download.microsoft.com/download/9/f/d/  
    9fd73f17-2fdf-4409-b2d2-31437c7f29f3/WLANCertEnroll.doc](http://download.microsoft.com/download/9/f/d/9fd73f17-2fdf-4409-b2d2-31437c7f29f3/wlancertenroll.doc)
  
(Este artículo contiene referencias a guías de otros productos y vínculos a sitios Web que sólo están disponibles en inglés.)
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 5: Creación de la infraestructura de seguridad de LAN inalámbricas
  
[](#elaab)[Información general](#elaab)  
[](#ekaab)[Requisitos previos del capítulo](#ekaab)  
[](#ejaab)[Preparación para la implementación](#ejaab)  
[](#eiaab)[Comprobación de la preparación para la instalación](#eiaab)  
[](#ehaab)[Instalación de IAS](#ehaab)  
[](#egaab)[Registro de IAS en Active Directory](#egaab)  
[](#efaab)[Configuración del servidor IAS principal](#efaab)  
[](#eeaab)[Implementación de la configuración en varios servidores IAS](#eeaab)  
[](#edaab)[Configuración de puntos de acceso inalámbrico](#edaab)  
[](#ecaab)[Resumen](#ecaab)  
[](#ebaab)[Referencias](#ebaab)
  
### Información general
  
En este capítulo se proporcionan instrucciones para la instalación y configuración del Servicio de autenticación de Internet (IAS) con el fin de proporcionar servicios del Servicio de usuario de acceso telefónico de autenticación remota (RADIUS) para una red de área local inalámbrica (WLAN) y la configuración de puntos de acceso inalámbricos para utilizar los servicios RADIUS de IAS.
  
Los temas principales del capítulo son los siguientes:
  
-   Preparación e instalación de IAS
  
-   Configuración del servidor IAS principal
  
-   Replicación de la configuración en otros servidores IAS
  
-   Adición de puntos de acceso inalámbrico como clientes RADIUS a IAS
  
-   Configuración de los puntos de acceso inalámbricos
  
Los procedimientos de este capítulo son menos automatizados que los de capítulos anteriores. Aunque se puede configurar IAS de forma programada, algunos valores de configuración no se pueden configurar utilizando Windows® Scripting Host ni herramientas de línea de comandos disponibles. El código de aplicaciones compilado suele ser menos accesible que las secuencias de comandos para aquellos usuarios que no son programadores. Por ese motivo, cuando un procedimiento no se ha podido convertir en secuencias de comandos, se siguen los pasos del manual para completarlo. Si desea automatizar la configuración de IAS mediante la interfaz Objetos de datos del servidor, consulte MSDN® en [http://msdn.microsoft.com](http://msdn.microsoft.com/). Para conocer la ubicación exacta de la información sobre este tema, consulte las referencias al final de este capítulo.
  
Los pasos de configuración descritos en este capítulo son mayormente manuales; este hecho tiene algunos aspectos positivos. En primer lugar, la interfaz de administración de IAS es fácil de utilizar y suele estar controlada por asistentes de configuración. En segundo lugar, los pasos de configuración se realizan normalmente en un único servidor y, más adelante, esta configuración se replica en los demás servidores IAS mediante unos sencillos comandos. En tercer lugar, la realización manual de estos pasos le ayudará a saber más sobre la instalación y configuración de IAS. Este último punto es más relevante para este componente de la solución que para los otros. IAS es el concentrador alrededor del cual gira el resto de la solución, por lo que es recomendable tener algo de experiencia en la administración y configuración del mismo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Requisitos previos del capítulo
  
Antes de implementar las instrucciones proporcionadas en este capítulo, debe leer e implementar los procedimientos del capítulo 3, "Preparación del entorno", y 4, "Creación de la entidad emisora de certificados de red". También debe leer el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas", y conocer la arquitectura y el diseño de esta solución.
  
Además, resultará útil que esté familiarizado con los siguientes temas:
  
-   IAS y RADIUS
  
-   Conceptos de WLAN
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Preparación para la implementación
  
#### Permisos necesarios
  
Para llevar a cabo los procedimientos de este capítulo, debe iniciar sesión con una cuenta que pertenezca al grupo de administradores del dominio en el que se van a instalar los servidores IAS.
  
**Nota:** si no va a instalar IAS en controladores de dominio, sólo deberá pertenecer al grupo de administradores locales en cada servidor IAS donde se va a instalar y configurar IAS. También deberá tener permisos para modificar la pertenencia al grupo Servidores RAS e IAS del dominio en el que se van a instalar los servidores IAS.
  
#### Herramientas necesarias
  
Para realizar los procedimientos de este capítulo son necesarias las siguientes herramientas.
  
**Tabla 5.1. Herramientas necesarias**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Herramienta</th>
<th style="border:1px solid black;" >Descripción</th>
<th style="border:1px solid black;" >Fuente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Secuencias de comandos para la seguridad en WLAN de MSS</td>
<td style="border:1px solid black;">Conjunto de secuencias de comandos y herramientas que se incluyen en esta solución.</td>
<td style="border:1px solid black;">Se proporciona en el capítulo 3, &quot;Preparación del entorno&quot;.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Servicio de autenticación de Internet</strong></td>
<td style="border:1px solid black;">Herramienta de Microsoft® Management Console (MMC) utilizada para administrar la configuración y las directivas de IAS.</td>
<td style="border:1px solid black;">Se proporciona como parte de Windows Server™ 2003.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Usuarios y equipos de Active Directory</strong></td>
<td style="border:1px solid black;">Herramienta de MMC utilizada para administrar los equipos, grupos y usuarios del servicio de directorio de Microsoft Active Directory®, así como otros objetos de Active Directory.</td>
<td style="border:1px solid black;">Se proporciona como parte de Windows Server 2003.</td>
</tr>
</tbody>
</table>
  
#### Parámetros de IAS
  
En la siguiente tabla se muestran los parámetros principales utilizados en la instalación y configuración del servidor IAS.
  
**Tabla 5.2. Parámetros de configuración del servidor IAS**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Elemento de configuración</th>
<th style="border:1px solid black;" >Valor de configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Registro IAS en el registro de sucesos de Windows</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Solicitudes de autenticación rechazadas</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Solicitudes de autenticación correctas</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Registro de RADIUS IAS</strong></td>
<td style="border:1px solid black;">Deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Directiva de acceso remoto</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Nombre de directiva de acceso remoto</td>
<td style="border:1px solid black;">Permitir acceso a LAN inalámbrica</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Grupo de seguridad al que se concede acceso</td>
<td style="border:1px solid black;">Acceso a LAN inalámbrica</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Tipo de EAP utilizado</td>
<td style="border:1px solid black;">Protocolo de autenticación extensible protegido (PEAP)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Tipo de PEAP utilizado</td>
<td style="border:1px solid black;">EAP MS-CHAP v2</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Reconexión rápida</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Perfil de directiva de acceso remoto</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Minutos que el cliente puede estar conectado (tiempo de espera de sesión)</td>
<td style="border:1px solid black;">60 minutos
Se puede reducir a 15 minutos para redes WLAN 802.11a/g de 54 Mbps</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Atributos de RADIUS</td>
<td style="border:1px solid black;">Ignorar propiedades de acceso telefónico del usuario = &quot;True&quot;
Acción-Terminación = &quot;RADIUS-Request&quot;</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Directiva de solicitud de conexión</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Nombre de directiva</td>
<td style="border:1px solid black;">Usar autenticación de Windows para todos los usuarios</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Condiciones de la directiva</td>
<td style="border:1px solid black;">Restricciones de fecha y hora = Todas las horas</td>
</tr>
</tbody>
</table>
  
**Importante:** esta configuración se utilizó en las pruebas internas de esta solución y su funcionamiento está garantizado tal y como se describe. Aunque se pueden modificar algunos valores de esta configuración, sólo debería hacerlo si está seguro de que comprende perfectamente la finalidad de un valor de configuración concreto y lo que implicaría su modificación.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Comprobación de la preparación para la instalación
  
IAS depende de la correcta configuración y conectividad de la red y de Active Directory. Para la instalación y el mantenimiento adecuados de IAS son necesarias varias herramientas.
  
#### Validación del entorno IAS
  
Antes de instalar IAS en el servidor, debe realizar una serie de comprobaciones para garantizar que puede ponerse en contacto con el controlador de dominio y que se han instalado todas las herramientas necesarias siguiendo los procedimientos descritos en el capítulo 3, "Preparación del entorno". El siguiente procedimiento utiliza una secuencia de comandos para realizar estas comprobaciones por usted de forma automática.
  
**Para comprobar el entorno IAS**
  
1.  Abra un shell de comandos utilizando el acceso directo **MSS WLAN Tools** que se encuentra en el servidor en el que desea instalar IAS.
  
2.  Ejecute el comando siguiente:
  
    **MSSSetup CheckIASEnvironment**
  
3.  La secuencia de comandos confirma el nombre del dominio al que pertenece el servidor. Haga clic en **Aceptar** para confirmar.
  
4.  Cuando finalice las comprobaciones, aparecerá un cuadro de diálogo indicando si cada una de ellas se ha realizado correctamente o no. Haga clic en **Aceptar** para cerrar el cuadro de diálogo.
  
5.  Si todas las comprobaciones se realizaron correctamente, continúe con el siguiente procedimiento. De lo contrario, compruebe el registro de instalación (**%systemroot%\\debug\\MSSWLAN-Setup.log**) para determinar la causa del error y corregir el problema antes de volver a ejecutar la secuencia de comandos.
  
#### Comprobación de la configuración de DHCP
  
El protocolo de configuración dinámica de host (DHCP) se utilizará para asignar automáticamente direcciones IP a los clientes WLAN. Asegúrese de que los ámbitos DHCP asignados en cada sitio disponen de suficientes direcciones IP para abarcar el máximo número posible de clientes WLAN que pueden estar activos en el sitio. Si el ámbito se comparte con clientes por cable, debe ser lo suficientemente grande como para dar cabida a ambos conjuntos de clientes.
  
Las organizaciones con un número elevado de clientes WLAN o que tengan clientes de WLAN que se desplacen regularmente de un sitio a otro, deben configurar ámbitos distintos para ellos. Al disponer de distintos ámbitos, se pueden especificar tiempos de concesión muy breves para dichos clientes (por ejemplo, ocho horas o menos) y, de esta forma, se evita que los clientes WLAN transitorios agoten las direcciones IP disponibles. Para ello, coloque a los clientes WLAN en una subred distinta de la red de sitios y configure un enrutador o un conmutador de nivel 3 para conectar las subredes.
  
En entornos pequeños o relativamente estáticos, la opción de compartir una subred IP y un ámbito DHCP único entre clientes por cable y de WLAN es bastante aceptable.
  
Para obtener más información, consulte el capítulo sobre la implementación de una LAN inalámbrica del *Kit de distribución de Microsoft Windows Server 2003*. La referencia del mismo se proporciona al final de este capítulo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Instalación de IAS
  
En esta sección se describe cómo instalar IAS en el servidor.
  
#### Instalación de componentes de software de IAS
  
Puede instalar los componentes de software de IAS utilizando la secuencia de comandos que se proporciona en esta guía. Esta secuencia de comandos utiliza el administrador de instalación de componentes opcionales de Windows para instalar IAS y crea todos los archivos de configuración necesarios a medida que se ejecuta.
  
**Para instalar IAS**
  
1.  Abra un shell de comandos utilizando el acceso directo **MSS WLAN Tools**.
  
2.  Ejecute el siguiente comando para instalar los componentes de software de IAS:
  
    **MSSSetup InstallIAS**
  
3.  La secuencia de comandos creará el archivo de parámetros de instalación. Cuando finalice esta operación, se le solicitará que continúe con la instalación. Necesitará el CD de instalación de Windows Server 2003 (o la ruta de red que contiene el origen de instalación de Windows) para finalizar la instalación. Haga clic en **Aceptar** para continuar o en **Cancelar** para detener la instalación antes de que finalice.
  
    **Nota:** si decide cancelar la instalación, el archivo de parámetros de componentes opcionales de IAS (OC\_IAS.txt) permanecerá en la carpeta de trabajo actual. Puede modificar la ubicación y usarla en la instalación personalizada si no desea aceptar los valores predeterminados de la solución.
  
4.  Cuando finalice la instalación, se mostrará un mensaje de confirmación. Haga clic en **Aceptar**.
  
#### Comprobación de la instalación
  
Para comprobar la instalación, haga clic en **Inicio**, elija **Todos los programas**, seleccione **Herramientas administrativas** y haga clic en **Servicio de autenticación de Internet**. IAS debe aparecer tal y como se instaló y ejecutándose en el servidor.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Registro de IAS en Active Directory
  
Todos los servidores IAS se deben registrar en Active Directory. Su registro significa la adición de la cuenta de equipo del servidor IAS para el grupo de seguridad Servidores RAS e IAS, lo que garantiza que los servidores IAS tengan permiso para leer las propiedades de acceso remoto de las cuentas de usuario y equipo en Active Directory.
  
Puede registrar los servidores de las siguientes maneras:
  
-   Al agregar manualmente los servidores al grupo (utilizando **Usuarios y equipos de Active Directory**).
  
-   Al utilizar el elemento **Registrar con Active Directory** del menú **Acción** de la MMC del **Servicio de autenticación de Internet**.
  
-   Al utilizar el comando **Netsh**.
  
Este último método (con el comando **Netsh**) se muestra en esta guía porque es fácil de ejecutar como secuencia de comandos y permite registrar el servidor en otros dominios.
  
**Para registrar IAS en el dominio predeterminado**
  
1.  Inicie sesión en el servidor IAS y abra un shell de comandos utilizando el acceso directo **MSS WLAN Tools**.
  
2.  Ejecute el comando siguiente:
  
    **netsh ras add registeredserver**
  
Si tiene varios dominios, realice el siguiente procedimiento para cada dominio con usuarios o equipos que vaya a autenticar este servidor IAS. Por ejemplo, si los servidores IAS se instalan en el dominio A y existen usuarios de WLAN en el dominio B, debe registrar los servidores en ambos dominios. Para ello, necesita tener permiso para modificar la pertenencia al grupo Servidores RAS e IAS en el dominio de destino.
  
**Para registrar IAS en un dominio que no es el predeterminado**
  
1.  En el símbolo del sistema, ejecute el siguiente comando y sustituya *NombreDominio* por el nombre del dominio en el que se debe registrar el servidor IAS:
  
    **netsh ras add registeredserver domain =** *NombreDominio*
  
    **Nota:** otra opción consiste en agregar el objeto de equipo del servidor IAS directamente al grupo de seguridad Servidores RAS e IAS en el dominio de destino utilizando **Usuarios y equipos de Active Directory**.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración del servidor IAS principal
  
En esta sección se proporcionan instrucciones para la configuración del servidor IAS principal. Los servidores IAS posteriores se configurarán mediante la replicación de la configuración de este servidor y utilizando los procedimientos descritos más adelante en este capítulo.
  
#### Inscripción automática de un certificado de servidor IAS
  
En el capítulo 4, "Creación de la entidad emisora de certificados de red", se proporcionaron los pasos que se deben seguir para instalar un objeto de directiva de grupo (GPO) con el fin de permitir a los miembros del grupo Servidores RAS e IAS inscribir automáticamente certificados de equipo. Al registrar el servidor IAS en Active Directory se agrega la cuenta del servidor a este grupo. Sin embargo, será necesario reiniciar el servidor para que el equipo pueda agregar este grupo al token de inicio de sesión y pueda inscribir un certificado correctamente.
  
**Nota:** al igual que ocurre con los usuarios, los equipos no reciben la modificación de la pertenencia de grupo en el token de acceso hasta que vuelven a iniciar sesión en el dominio. En los equipos, esto ocurre durante el inicio.
  
Antes de continuar con el siguiente procedimiento, reinicie el servidor.
  
**Advertencia:** antes de reiniciar el servidor, asegúrese de que no se está realizando ninguna tarea en el mismo. Si el servidor es un controlador de dominio, asegúrese de que dispone de otro controlador para los usuarios antes de reiniciar el primero. También debe evitar su reinicio durante la realización de una tarea importante del sistema, como por ejemplo, la copia de seguridad del servidor.
  
##### Comprobación de la implementación de certificados de servidores IAS
  
Después de reiniciar el servidor, asegúrese de que el certificado de servidor IAS se ha inscrito correctamente.
  
**Para comprobar el certificado de autenticación de servidor IAS**
  
1.  Abra un shell de comandos utilizando el acceso directo **MSS WLAN Tools**.
  
2.  Ejecute el siguiente comando para abrir la MMC de **Certificados**:
  
    **ComputerCerts.msc**
  
3.  En el árbol de la consola, haga doble clic en **Certificados (equipo local)** y en **Personal**. A continuación, haga clic en **Certificados**.
  
4.  Debe aparecer al menos un certificado con el nombre de este servidor en la columna **Emitido para** y el nombre de la entidad emisora de certificados en la columna **Emitido por**. Desplácese por la lista (situada a la derecha) para ver la columna **Plantilla de certificado**. Debe aparecer el valor **Equipo** para este certificado en esta columna.
  
    **Nota:** si éste es el servidor IAS principal y se está instalando en el mismo servidor que la entidad emisora, aparecerá también otro certificado con el nombre de la entidad emisora en ambas columnas; éste es el certificado de entidad emisora con firma personal.
  
5.  Si el certificado necesario no aparece en el complemento MMC de **Certificados**, seleccione **Certificados (equipo local)** en el árbol de la consola (en el panel izquierdo), haga clic en **Todas las tareas** en el menú **Acción** y, a continuación, seleccione **Inscribir certificados automáticamente**. A continuación, actualice la vista de la MMC de **Certificados**.
  
#### Configuración del servidor IAS principal
  
La configuración de todos los servidores IAS será muy parecida en esta solución (aunque el conjunto de puntos de acceso inalámbrico instalado en cada servidor normalmente será distinto para cada uno de ellos). Para mantener la configuración sincronizada entre los servidores y para reducir el esfuerzo que supone administrar varios servidores, realizará la mayoría de las tareas de configuración en el servidor IAS principal instalado y, a continuación, replicará la configuración de este servidor en los demás servidores IAS de la organización.
  
Durante los procedimientos de esta sección, configurará los siguientes tipos de valor de configuración en el servidor IAS principal:
  
-   Registro de solicitudes
  
-   Directiva de acceso remoto
  
-   Configuración de solicitudes de conexión
  
Más adelante, se replicará esta configuración en los demás servidores IAS. También debe agregar una entrada de cliente RADIUS a IAS para cada punto de acceso inalámbrico procesado mediante ese servidor IAS (lo que se explica en la sección "Configuración de puntos de acceso inalámbrico", más adelante en este capítulo).
  
##### Configuración del registro en el registro de sucesos de Windows
  
IAS registra los sucesos importantes del sistema, como por ejemplo, el inicio y cierre del servicio, y problemas tales como los errores de configuración y de servicio en el registro del sistema Windows. También puede registrar, opcionalmente, los intentos de autenticación tanto correctos como erróneos.
  
**Para habilitar el registro de las solicitudes de autenticación en IAS**
  
1.  Abra la MMC del **Servicio de autenticación de Internet**, haga clic en **Inicio**, elija **Todos los programas**, seleccione **Herramientas administrativas** y haga clic en **Servicio de autenticación de Internet**.
  
2.  Haga clic con el botón secundario en **Servicio de autenticación de Internet (local)** y, a continuación, seleccione **Propiedades**.
  
3.  Asegúrese de que **Solicitudes de autenticación rechazadas** y **Solicitudes de autenticación correctas** están habilitadas.
  
4.  Haga clic en **Aceptar**.
  
##### Configuración del registro de solicitudes de autenticación y de cuentas en registros RADIUS
  
IAS también puede registrar información de autenticación y de cuentas en registros RADIUS. IAS no crea registros RADIUS de forma predeterminada y no se ha habilitado el registro RADIUS en esta solución con el fin de reducir la carga de administración.
  
Si necesita el registro RADIUS con fines de administración de cuentas o auditorías de seguridad, es posible habilitar uno o ambos tipos de registros de solicitudes. IAS puede escribir estos registros en archivos de texto o en una base de datos SQL. Puede utilizar estos registros como entrada para los sistemas de supervisión de seguridad con el fin de realizar un seguimiento de posibles infracciones de seguridad. Menos frecuente es el uso por parte de las organizaciones de los registros de cuentas para la facturación, aunque esto suele estar confinado a los proveedores comerciales de servicios de Internet y otros de servicios de red. Si desea implementar el registro RADIUS o simplemente obtener más información sobre él, consulte las referencias al final de este capítulo.
  
**Nota:** no debe habilitar el registro de solicitudes de autenticación y de cuentas RADIUS a menos que exista un motivo específico para hacerlo. Puede afectar al rendimiento del servidor y además es necesario el mantenimiento regular de los archivos de registro para garantizar que no llenan los discos del servidor.
  
##### Creación de una directiva de acceso remoto IAS para WLAN
  
Realice el siguiente procedimiento para crear una directiva de acceso remoto en el servidor IAS.
  
**Para crear una directiva de acceso remoto en IAS**
  
1.  En la MMC del **Servicio de autenticación de Internet**, haga clic en **Inicio**, elija **Todos los programas**, seleccione **Herramientas administrativas** y haga clic en **Servicio de autenticación de Internet**.
  
2.  Haga clic con el botón secundario en la carpeta **Directivas de acceso remoto** y, a continuación, haga clic en **Nueva directiva de acceso remoto**. Haga clic en **Siguiente** para continuar.
  
3.  Seleccione **Directiva típica para un escenario común** como el modo en que desea configurar la directiva y asígnele el nombre **Permitir acceso a LAN inalámbrica**. Haga clic en **Siguiente**.
  
4.  Seleccione **Inalámbrico** como método de acceso.
  
5.  Seleccione la opción **Grupo** para **Conceder acceso basado en** y escriba (o busque) el grupo de seguridad Acceso a LAN inalámbrica. Haga clic en **Siguiente** para continuar.
  
6.  Seleccione **EAP protegido (PEAP)** en la lista de tipos de EAP.
  
7.  Haga clic en el botón **Configurar**. El certificado de servidor IAS emitido anteriormente debe mostrarse en el campo **Certificado emitido** (si no es así, selecciónelo de la lista de certificados disponibles). **Contraseña segura (EAP MSCHAPv2)** debe aparecer en la lista **Tipos de EAP**. Compruebe la casilla de verificación **Habilitar** **reconexión rápida**.
  
    **Importante:** si utiliza clientes inalámbricos con Pocket PC 2003, no debe activar la casilla de verificación **Habilitar reconexión rápida** a menos que tenga una versión de Pocket PC que sea compatible con esta opción (consulte la referencia del artículo de Knowledge Base al final de este capítulo). Si habilita la reconexión rápida, los clientes con Pocket PC no podrán volver a conectarse a la red una vez transcurrido el tiempo de espera de la autenticación inicial.
  
8.  Haga clic en **Aceptar** y, a continuación, en **Siguiente**. Haga clic en **Finalizar** para completar el procedimiento.
  
    **Importante:** la nueva directiva **Permitir** **acceso** **a LAN** **inalámbrica** puede coexistir con otras directivas de acceso remoto que haya creado o con las directivas de acceso remoto predeterminadas. Sin embargo, debe asegurarse de que cualquier otra directiva de acceso remoto predeterminada se elimina o se enumera (en una prioridad inferior) después de la directiva **Permitir acceso a LAN inalámbrica** en la carpeta **Directivas de acceso remoto** de IAS.
  
##### Modificación de la configuración del perfil de la directiva de acceso a WLAN
  
El asistente para **Nueva directiva de acceso remoto** (según se ha utilizado en el procedimiento anterior) crea una directiva de acceso remoto válida, pero los dos siguientes valores se deben configurar de forma manual. La primera agrega el atributo de RADIUS **Ignorar propiedades de acceso telefónico del usuario**. De este modo se indica a IAS que ignore el valor de configuración de permiso de acceso remoto que se especifica en la ficha **Acceso telefónico** del objeto de usuario de Active Directory. También se evita que IAS envíe esta información en las respuestas de RADIUS a los puntos de acceso inalámbrico, ya que en algunas ocasiones puede causar problemas de compatibilidad.
  
La segunda categoría permite que el servidor IAS termine la conexión del cliente una vez transcurrido el tiempo de vigencia especificado y forzar al cliente a reautenticarse. Esta configuración es particularmente importante cuando se utiliza la protección de datos mediante la privacidad equivalente por cable (WEP) dinámica (la opción predeterminada para esta solución). El tiempo de espera de la sesión controla la frecuencia con la que se generan nuevas claves de red de cifrado de datos.
  
**Nota:** el acceso protegido Wi-Fi (WPA) tiene su propio mecanismo para generar nuevas claves para cada paquete transmitido. El siguiente tema no se aplica a WLAN con WPA.
  
El valor de tiempo de espera de sesión es un equilibrio entre seguridad y confiabilidad. Un tiempo de espera de 60 minutos proporciona una seguridad adecuada para la mayoría de las circunstancias y, con seguridad, para las redes 802.11b de 11 Mbps. Normalmente, los clientes inalámbricos nunca transmitirán datos suficientes en 60 minutos como para permitir que un atacante recupere una clave WEP dinámica. Las WLAN más rápidas que utilizan estándares 802.11a o 802.11g de 54 Mbps permiten la transmisión de una mayor cantidad de datos en un tiempo determinado; debe considerar el uso de un tiempo de espera de 15 minutos para estas redes. Si utiliza un valor inferior, puede reducir la confiabilidad de la WLAN y aumentar la carga en los servidores IAS.
  
Debe consultar la sección "Opciones de seguridad para la WEP dinámica" del capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas" para obtener información más detallada sobre la configuración del tiempo de espera de sesión del cliente.
  
Debe configurar el tiempo de espera de sesión del cliente y el atributo **Acción-Terminación** de RADIUS en el valor adecuado de manera que el servidor IAS pueda forzar al cliente a reautenticarse en el intervalo necesario. Para obtener más información sobre la configuración de directivas de acceso remoto, consulte la sección "Directivas de RADIUS" del capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas".
  
**Para modificar la configuración del perfil de la directiva de acceso inalámbrico**
  
1.  En la MMC del **Servicio de autenticación de Internet**, haga clic con el botón secundario en la directiva **Permitir acceso a LAN inalámbrica** y seleccione **Propiedades**. A continuación, haga clic en **Modificar perfil**.
  
2.  Haga clic en la ficha **Restricciones de marcado** y, a continuación, seleccione la opción **Minutos que el cliente puede estar conectado (tiempo de espera de sesión)** y escriba el valor **60** (minutos) si utiliza una WLAN 802.11b (de 11 Mbps) o **15** (minutos) si utiliza una WLAN 802.11a de velocidad superior o una 802.11g (de 54 Mbps).
  
    **Nota:** si utiliza una WLAN con protección WPA en lugar de WEP dinámica, establezca este valor en ocho horas. Un valor de ocho horas garantizará que los clientes tengan unas credenciales actualizadas válidas para un período de tiempo razonable. Al mismo tiempo, garantizará que un cliente no pueda permanecer conectado durante períodos de tiempo excesivos una vez desactivada la cuenta. Sin embargo, en entornos de alta seguridad donde es necesario reducir el tiempo de retraso entre desactivar una cuenta y forzar al cliente a desactivarse de la red, este valor se puede disminuir a una hora.
  
3.  Haga clic en la ficha **Avanzadas**, agregue el atributo **Ignorar propiedades de acceso telefónico del usuario** y establézcalo en **True**. A continuación, agregue el atributo **Acción-Terminación** y establézcalo en **RADIUS Request**.
  
##### Comprobación de la directiva de solicitud de conexión para WLAN
  
La directiva de solicitud de conexión IAS predeterminada está configurada para indicar a IAS que autentique los usuarios y los clientes directamente en Active Directory. Lleve a cabo los pasos siguientes para comprobar la configuración de la directiva de solicitud de conexión predeterminada.
  
**Para comprobar la configuración de la directiva de solicitud de conexión predeterminada**
  
1.  Abra la MMC del **Servicio de autenticación de Internet**, vaya hasta la carpeta **Procesamiento solicitud de conexión\\Directivas de solicitud de conexión** y haga clic con el botón secundario en la directiva de solicitud de conexión **Usar autenticación de Windows para todos los usuarios**. A continuación, seleccione **Propiedades**.
  
2.  Compruebe que las condiciones de la directiva contienen **Coincidencias de restricciones de fecha y hora"Dom 00:00-24:00; Lun 00:00-24:00; Mar 00:00-24:00; Mié 00:00-24:00; Jue 00:00-24:00; Vie 00:00-24:00; Sáb 00:00-24:00"**.
  
3.  Haga clic en el botón **Modificar perfil** y asegúrese de que ha seleccionado **Autenticar solicitudes en este servidor** en la ficha **Autenticación**.
  
4.  Asegúrese de que no hay reglas especificadas en la ficha **Atributo**.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Implementación de la configuración en varios servidores IAS
  
Después de configurar el servidor IAS principal, puede replicar esta configuración en los demás servidores IAS.
  
Repita los procedimientos anteriores de este capítulo para la "Instalación de IAS" y el "Registro de IAS en Active Directory" en cada uno de los servidores adicionales. También debe realizar el procedimiento de "Comprobación de la implementación de certificados de servidores IAS" para garantizar que se ha inscrito un certificado por cada nuevo servidor. Una vez realizados estos procedimientos, estará listo para exportar la configuración de IAS del servidor principal e importarla a los demás servidores, tal y como se describe en los procedimientos de la siguiente sección.
  
**Importante:** sólo puede replicar la configuración a otros servidores IAS de Windows Server 2003. Con estos procedimientos, no puede replicar la configuración de IAS desde versiones de Windows Server 2003 a otras de Windows 2000.
  
#### Replicación de la configuración desde el servidor IAS principal
  
Puede utilizar el comando **Netsh** para exportar parte de la configuración de IAS a archivos de texto. Las secuencias de comandos utilizadas en los siguientes procedimientos utilizan Netsh.exe para exportar la configuración de un servidor IAS e importarla a otro.
  
Las siguientes categorías de configuración de IAS se pueden exportar por separado de un servidor IAS e importar a otro servidor IAS:
  
-   Configuración de servidor
  
-   Configuración de registro
  
-   Directivas de acceso remoto
  
-   Directivas de solicitud de conexión
  
-   Clientes RADIUS
  
-   Configuración completa (incluye todo lo anterior)
  
La configuración exportada se almacena en archivos de texto, aunque los datos estén codificados. Estos archivos de texto se pueden utilizar para transferir la configuración habitual a varios servidores IAS con el fin de garantizar una configuración coherente y una implementación rápida.
  
La mayoría de las categorías de configuración serán comunes a los servidores IAS con una función similar (normalmente con la excepción de la categoría de clientes RADIUS). En esta solución, los servidores IAS autenticarán únicamente clientes WLAN. Si tiene previsto utilizar uno o varios servidores IAS de forma diferente (por ejemplo, para autenticar clientes de acceso remoto), tendrá que configurar y replicar la configuración de estos servidores de manera independiente o realizar la configuración manualmente. De lo contrario, correrá el riesgo de sobrescribirla y perder valores de directivas y otros valores de configuración.
  
La configuración de los siguientes elementos sólo debe realizarse en el servidor IAS principal (tal y como se describe en la sección anterior "Configuración de IAS").
  
-   Configuración del servidor
  
-   Configuración de registro
  
-   Directivas de acceso remoto
  
-   Directivas de solicitud de conexión
  
Esta configuración se exportará mediante los procedimientos de esta sección y se replicará en los otros servidores IAS.
  
**Sugerencia:** para que sea más fácil realizar un seguimiento de los cambios realizados en la configuración de IAS, incluya un número de versión en el nombre de la directiva de acceso remoto. Cada vez que modifique la configuración de IAS, actualice el nombre de manera que incluya un nuevo número de versión. De este modo será más sencillo realizar un seguimiento de los cambios realizados en los servidores IAS y comprobar si todos están utilizando la misma configuración.
  
Designe el servidor IAS principal como servidor IAS "maestro". A continuación, utilice los siguientes procedimientos para replicar la configuración de este servidor en otros servidores IAS de la organización. La replicación de la configuración de clientes RADIUS se detalla en la sección "Replicación de la configuración de clientes RADIUS en otros servidores IAS" más adelante en este capítulo.
  
**Nota:** la designación de "maestro" no tiene ningún significado especial para IAS. Sólo se utiliza para indicar el servidor que se usará para realizar los cambios de la configuración inicial antes de replicarla en otros servidores IAS.
  
##### Exportación de la configuración del servidor IAS maestro
  
Este procedimiento guarda la configuración actual del servidor IAS en los archivos de disco.
  
**Para exportar la configuración de IAS a archivos de disco**
  
1.  Inicie sesión en el servidor IAS principal y abra un shell de comandos utilizando el acceso directo **MSS WLAN Tools**.
  
2.  Si es necesario, identifique una carpeta para almacenar los archivos de salida o inserte un disco formateado vacío en la unidad del servidor.
  
3.  Ejecute el siguiente comando para exportar la configuración de IAS:
  
    **MSSTools ExportIASSettings** \[**/path:***CarpetaSalida*\]
  
    *CarpetaSalida* es un parámetro opcional utilizado para especificar la carpeta en la que se escribirán los archivos exportados. La ruta debe estar escrita entre comillas si incluye espacios. Esta carpeta, si se especifica, debe existir o de lo contrario, los archivos se escribirán en el directorio actual.
  
4.  La secuencia de comandos creará los siguientes archivos:
  
    -   IAS\_Server\_Settings.txt
  
    -   IAS\_Logging.txt
  
    -   IAS\_Rem\_Access\_Policies.txt
  
    -   IAS\_Con\_Request\_Policies.txt
  
5.  Almacene los archivos para importarlos a los demás servidores.
  
##### Importación de la configuración a otros servidores IAS
  
Este procedimiento utiliza los archivos de configuración exportados en el procedimiento anterior para configurar otros servidores IAS con la misma configuración. Este procedimiento no importa los clientes RADIUS, lo cual se explica en una sección posterior.
  
**Advertencia:** la importación de la configuración de IAS a otro servidor IAS sobrescribirá la configuración de IAS existente en dicho servidor (excepto la información de clientes RADIUS). Si ha creado diferentes configuraciones en un servidor (por ejemplo, diferentes directivas de acceso remoto para admitir clientes de una red privada virtual, VPN), no utilice este procedimiento para importar la configuración de WLAN de IAS a este servidor. En su lugar, establezca la configuración manualmente mediante los procedimientos descritos en la sección "Configuración del servidor IAS principal" anteriormente en este capítulo.
  
**Para importar la configuración IAS desde archivos de disco**
  
1.  Inicie sesión en el servidor IAS de destino y abra un shell de comandos mediante el acceso directo **MSS WLAN Tools**.
  
2.  Identifique la carpeta que contiene los archivos de configuración exportados previamente desde el servidor IAS maestro.
  
3.  Ejecute el siguiente comando para importar la configuración de IAS:
  
    **MSSTools ImportIASSettings** \[**/path:***CarpetaEntrada*\]
  
    *CarpetaEntrada* es un parámetro opcional que se utiliza para especificar la carpeta en la que la secuencia de comandos buscará los archivos de configuración que va a importar. La ruta debe estar escrita entre comillas si incluye espacios. Si no se especifica ninguna carpeta, los archivos deberán encontrarse en el directorio actual.
  
Debe comprobar que la configuración se ha importado correctamente abriendo la MMC del **Servicio de autenticación de Internet** y comprobando la configuración de las directivas de solicitud de conexión y acceso remoto.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de puntos de acceso inalámbrico
  
En esta sección se describe cómo agregar puntos de acceso inalámbrico como clientes RADIUS a los servidores IAS.
  
#### Adición de puntos de acceso como clientes RADIUS a IAS
  
Debe agregar puntos de acceso inalámbrico como clientes RADIUS a IAS para que se les permita utilizar los servicios de autenticación y cuentas RADIUS. Para obtener más información sobre cómo asignar puntos de acceso inalámbrico a diferentes servidores IAS, consulte los procedimientos del capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas".
  
Los puntos de acceso inalámbrico de una ubicación concreta se configurarán de la forma habitual para que utilicen un servidor IAS de la misma ubicación para el servidor RADIUS principal y otro servidor IAS de la misma u otra ubicación para el servidor RADIUS secundario. Los términos "principal" y "secundario" no hacen referencia a una relación jerárquica ni a una diferencia de configuración entre los propios servidores IAS. Los términos son relevantes sólo para los puntos de acceso inalámbrico, cada uno de los cuales tiene designados un servidor RADIUS principal y secundario (o de copia de seguridad). Antes de configurar los puntos de acceso inalámbrico, debe decidir qué servidor IAS será el servidor RADIUS principal y cuál será el secundario para cada punto de acceso.
  
En los procedimientos siguientes se describe cómo agregar clientes RADIUS a dos servidores IAS. Durante el primer procedimiento se crea un secreto de RADIUS para el punto de acceso inalámbrico; IAS y el punto de acceso inalámbrico utilizarán este secreto o clave para autenticarse entre sí. Los detalles de este cliente, junto con su secreto, se registran en un archivo. Este archivo se utiliza en el segundo procedimiento para importar el cliente al IAS secundario.
  
**Importante:** no use este primer procedimiento para agregar el mismo cliente a dos servidores IAS. Si lo hace, las entradas del cliente de cada servidor tendrán configurados diferentes secretos de RADIUS y el punto de acceso inalámbrico no podrá autenticarse en ambos servidores.
  
##### Adición de puntos de acceso al servidor IAS principal
  
En esta sección se describe cómo agregar puntos de acceso inalámbrico al servidor IAS principal. Se proporciona una secuencia de comandos para automatizar la creación de un secreto (contraseña) seguro y aleatorio de RADIUS, y agregar el cliente a IAS. La secuencia de comandos también crea un archivo (de forma predeterminada es Clients.txt) que registra los detalles de cada punto de acceso inalámbrico agregado. Este archivo registra el nombre, la dirección IP y el secreto de RADIUS creados para cada punto de acceso inalámbrico. Estos datos serán necesarios para configurar el servidor IAS secundario y los puntos de acceso inalámbrico.
  
Si prefiere agregar los clientes manualmente, siga el procedimiento "Creación de entradas del cliente para puntos de acceso inalámbrico", descrito más adelante en este capítulo, para crear secretos para los puntos de acceso inalámbrico.
  
**Importante:** los clientes RADIUS se agregan a IAS como clientes "RADIUS estándar". Aunque resulta adecuado para la mayoría de los puntos de acceso inalámbrico, puede que algunos puntos de acceso requieran la configuración de atributos específicos del proveedor (VSA) en el servidor IAS. Puede configurar VSA seleccionando un dispositivo de proveedor específico en las propiedades de los clientes RADIUS en la MMC del **Servicio de autenticación de Internet** o (si no aparece el dispositivo) especificando los VSA en la directiva de acceso remoto de IAS. Para obtener más información sobre la configuración de VSA en IAS, consulte las referencias al final de este capítulo.
  
Asimismo, consulte la documentación sobre puntos de acceso inalámbrico para obtener información relacionada con los requisitos de VSA en servidores RADIUS.
  
**Para agregar un cliente RADIUS al servidor IAS principal**
  
1.  Inicie sesión en el servidor IAS al que desea agregar el punto de acceso inalámbrico y abra un shell de comandos utilizando el acceso directo **MSS WLAN Tools**.
  
2.  Si ya hay un archivo de salida de clientes RADIUS en el directorio actual (o si especifica un archivo existente en el parámetro de ruta), la nueva entrada de cliente se agregará a dicho archivo. Si no desea que esto ocurra, elimine el archivo existente o especifique un nombre de archivo alternativo en el comando.
  
3.  Ejecute el siguiente comando para agregar un punto de acceso inalámbrico a IAS:
  
    **MSSTools AddRADIUSClient** \[**/path:***ArchivoSalida.txt*\]
  
    **Nota:** el parámetro de ruta *path* es opcional. Puede especificar el nombre del archivo (más una ruta de carpeta opcional) donde se almacenará el resultado del comando. La ruta debe estar escrita entre comillas si incluye espacios. Si no se especifica ningún parámetro de ruta, el comando guardará el resultado en el archivo Clients.txt en el directorio actual.
  
4.  Cuando se le indique, escriba un nombre para el punto de acceso inalámbrico. Éste debe ser una referencia descriptiva para la MMC del **Servicio de autenticación de Internet** y no tiene por qué ser necesariamente el nombre que se le ha asignado en la configuración del punto de acceso inalámbrico. Utilice el nombre de un sistema de nombre de dominio (DNS) o cualquier otra cadena.
  
5.  Escriba la dirección IP del punto de acceso inalámbrico (en notación decimal con punto; por ejemplo, 10.20.1.153).
  
6.  Se creará una contraseña automáticamente para el cliente (esta contraseña es una cadena cifrada de 23 caracteres imprimibles creada de forma aleatoria, que utilizan IAS y el punto de acceso inalámbrico para autenticarse entre sí). Esta configuración se utiliza para agregar el cliente RADIUS a IAS. El nombre, la dirección IP y el secreto también se agregan al archivo de salida (el predeterminado es Clients.txt) en el directorio actual. El archivo de salida es un archivo de texto delimitado por comas con un cliente RADIUS en cada línea, por lo que se puede utilizar fácilmente en secuencias de comandos o importar y manipular empleando una herramienta como Microsoft Excel.
  
7.  Repita los pasos 3 a 6 para todos los puntos de acceso inalámbrico que desee agregar a este servidor IAS.
  
Más adelante, utilizará el archivo de salida como referencia al establecer los secretos de RADIUS en los puntos de acceso inalámbrico. Para obtener más información, consulte la sección "Configuración de puntos de acceso inalámbrico" más adelante en este capítulo.
  
**Importante:** no deje el archivo de salida de clientes RADIUS en el servidor. Contiene los secretos de los clientes RADIUS sin cifrar. Después de agregar los puntos de acceso inalámbrico, debe mover el archivo a un disco u otro medio extraíble con permiso de escritura y almacenarlo en un lugar seguro.
  
El procedimiento de "Adición de clientes RADIUS al servidor IAS principal" descrito anteriormente utiliza una herramienta de ejemplo que se incluye en esta solución (AddRADIUSClient.exe*)*. Esta herramienta es una aplicación de Visual Basic.NET sencilla que utiliza la interfaz Objetos de datos de servidor para configurar un servidor IAS. Puede utilizarla para escribir su propia secuencia de comandos con el fin de agregar clientes al servidor IAS.
  
Esta herramienta no es compatible con Microsoft y no se ha probado minuciosamente. Sin embargo, el código fuente de esta aplicación se ha incluido en caso de que necesite examinarlo o modificarlo antes de su uso.
  
**Nota:** a diferencia de la mayoría de las secuencias de comandos utilizadas en los procedimientos de configuración, esta secuencia no escribe los detalles del progreso en el archivo de registro MSSWLAN-setup.log. El motivo es evitar que se almacenen allí los secretos de los clientes RADIUS, lo que conllevaría un riesgo de seguridad. Sin embargo, los detalles del progreso se registran en la pantalla.
  
###### Secuencias de comandos de la adición de puntos de acceso a un servidor IAS (procedimiento alternativo)
  
Si no desea agregar puntos de acceso inalámbrico al servidor IAS de forma interactiva utilizando el procedimiento anterior, puede simplemente crear los archivos de salida de las entradas de clientes RADIUS para cada punto de acceso inalámbrico sin agregarlos a IAS. Entonces podrá utilizar el procedimiento de "Importación de clientes RADIUS al servidor IAS secundario" descrito más adelante en esta sección para importar las entradas de clientes RADIUS tanto al servidor IAS principal como al secundario. Como esta operación entera se puede convertir en secuencias de comandos, quizás prefiera agregar los clientes RADIUS de este modo, si tiene que agregar un elevado número de puntos de acceso inalámbrico.
  
**Importante:** este procedimiento es un método alternativo para agregar clientes RADIUS por secuencias de comandos, en lugar de hacerlo de un modo interactivo. Si ha seguido el procedimiento anterior de "Adición de clientes RADIUS al servidor IAS principal", no tendrá que seguir este otro.
  
Utilice el siguiente procedimiento para crear secretos de RADIUS seguros. La secuencia de comandos, al igual que el procedimiento anterior, utiliza una función CryptoAPI para crear un valor totalmente aleatorio para cada secreto de RADIUS. De este modo se garantiza que los valores serán lo suficientemente seguros como para evitar ataques de averiguación de la contraseña o de diccionario.
  
**Para crear el archivo de entrada de clientes para puntos de acceso inalámbrico**
  
1.  Abra un shell de comandos utilizando el acceso directo **MSS WLAN Tools**.
  
2.  Ejecute el comando siguiente. Sustituya un nombre descriptivo del punto de acceso inalámbrico por el parámetro *NombreCliente* y la dirección IP del mismo por *DirecciónIP*. También puede proporcionar un nombre y una ruta de archivo alternativos para especificar dónde se van a guardar los datos de salida. Si no se especifica ningún parámetro de ruta, los datos de salida se guardarán en el archivo Clients.txt en la carpeta de trabajo actual. Si el archivo de salida ya existe, el nuevo valor se agregará al mismo. Si no existe, se creará.
  
    **MSSTools GenRADIUSPwd /client:***NombreCliente***/IP:***DirecciónIP* \[**/path:***ruta\\nombrearchivo*\]
  
    Los parámetros "client" y "path" pueden incluir espacios; si alguno de ellos los tiene, debe ponerlo entre comillas. El comando puede aparecer dividido en varias líneas, pero deberá escribirlo en una sola línea.
  
3.  Repita el paso 2 para todos los puntos de acceso inalámbrico para los que necesita crear secretos de RADIUS. Cada entrada de cliente se agregará al archivo de salida (el predeterminado es Clients.txt). El archivo es un archivo de texto delimitado por comas con un cliente RADIUS en cada línea, por lo que se puede utilizar fácilmente en secuencias de comandos o importar y manipular empleando una herramienta como puede ser Microsoft Excel.
  
    **Precaución:** no deje el archivo de salida en el servidor. Contiene los secretos de los clientes RADIUS sin formato. Después de agregar los puntos de acceso inalámbrico, debe mover el archivo a un disco u otro medio extraíble con permiso de escritura y almacenarlo en un lugar seguro.
  
    **Nota:** a diferencia de la mayoría de las secuencias de comandos utilizadas en los procedimientos de configuración, esta secuencia no escribe los detalles del progreso en el archivo de registro MSSWLAN-setup.log. El motivo es evitar que se almacenen allí los secretos de los clientes RADIUS, lo que conllevaría un riesgo de seguridad. Sin embargo, los detalles del progreso se registran en la pantalla.
  
##### Importación de puntos de acceso en el servidor IAS secundario
  
Después de agregar los puntos de acceso inalámbrico al servidor IAS principal, tiene que agregarlos a un servidor secundario antes de configurarlos para utilizar RADIUS.
  
**Para importar un cliente RADIUS al servidor IAS secundario**
  
1.  Copie el archivo de salida de clientes creado en los procedimientos anteriores (por motivos de seguridad, elimine por completo este archivo del servidor IAS principal; allí ya no es necesario).
  
2.  Compruebe que el archivo contiene las entradas correctas abriéndolo y viéndolo en Bloc de notas o Microsoft Excel. Esta acción es importante, ya que el archivo podría contener entradas antiguas que hayan quedado de una ejecución anterior del procedimiento. Elimine cualquier entrada de cliente que no sea necesaria.
  
3.  Ejecute el siguiente comando para importar estos clientes al servidor IAS secundario:
  
    **MSSTools AddSecRADIUSClients** \[**/path:***ArchivoEntrada.txt*\]
  
    **Nota:** el parámetro de ruta *path* es opcional. Puede utilizar otro parámetro de ruta para leer la entrada desde un archivo o una carpeta diferente. La ruta debe estar escrita entre comillas si incluye espacios. Si no se especifica ningún parámetro, el comando buscará y leerá la entrada del archivo Clients.txt en el directorio actual.
  
4.  La secuencia de comandos rechazará cualquier entrada de cliente mal formada y mostrará el número de entradas correctas e incorrectas al final.
  
5.  Compruebe que los clientes se han agregado correctamente. Para ello, abra la MMC del **Servicio de autenticación de Internet** y consulte la carpeta **Clientes RADIUS**.
  
    **Nota:** a diferencia de la mayoría de las secuencias de comandos utilizadas en la instalación y configuración de la solución, esta secuencia no escribe los detalles del progreso en el archivo MSSWLAN-setup.log. El motivo es evitar que se almacenen allí los secretos de los clientes RADIUS, lo que conllevaría un riesgo de seguridad. Sin embargo, los detalles del progreso se registran en la pantalla.
  
#### Configuración de puntos de acceso inalámbrico
  
Una vez agregadas las entradas de clientes RADIUS para los puntos de acceso inalámbrico a IAS, es necesario que configure dichos puntos de acceso. Asimismo, debe agregar las direcciones IP de los servidores IAS y los secretos de clientes RADIUS que utilizará cada punto de acceso para comunicarse con estos servidores de forma segura. Cada punto de acceso inalámbrico se configurará con un servidor IAS principal y uno secundario (o de copia de seguridad). Debe realizar los procedimientos de esta sección para los puntos de acceso inalámbrico en cada sitio de la organización. Para obtener más información sobre cómo asignar puntos de acceso inalámbrico a los servidores IAS, consulte el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas".
  
El procedimiento para configurar puntos de acceso inalámbrico varía según la marca y el modelo del dispositivo. Sin embargo, los proveedores de puntos de acceso inalámbrico ofrecen por lo general instrucciones detalladas para configurar sus dispositivos. Dependiendo del proveedor, estas instrucciones también pueden estar disponibles en línea.
  
Antes de establecer la configuración de seguridad para los puntos de acceso inalámbrico, debe establecer la configuración de red básica. Entre ellas se incluyen las siguientes:
  
-   Dirección IP y máscara de subred del punto de acceso inalámbrico
  
-   Puerta de enlace predeterminada
  
-   Nombre descriptivo del punto de acceso inalámbrico
  
-   Nombre de red inalámbrica (SSID)
  
Esta lista incluirá otros parámetros que afectan a la implementación de varios puntos de acceso inalámbrico: valores de configuración que controlan el alcance de radio correcto en todo el sitio; por ejemplo, canal de radio 802.11, velocidad y potencia de transmisión, etc. La explicación de estos parámetros no entra en el ámbito de esta guía. Utilice la documentación del proveedor como referencia cuando establezca esta configuración o consulte a un proveedor de servicios de red. Para obtener más información sobre la implementación de puntos de acceso inalámbrico, consulte las referencias al final de este capítulo.
  
Las instrucciones de este capítulo consideran que ha establecido estos elementos correctamente y que puede conectarse al punto de acceso inalámbrico desde un cliente WLAN utilizando una conexión no autenticada. Debe probar estas condiciones antes de configurar los parámetros de autenticación y seguridad que se enumeran en las siguientes secciones.
  
##### Habilitación de autenticación de seguridad de WLAN en puntos de acceso
  
Debe configurar cada punto de acceso inalámbrico con un servidor RADIUS principal y secundario. El punto de acceso utilizará por lo general el servidor principal para todas las solicitudes de autenticación y pasará al secundario si el principal no está disponible. Como se ha explicado en el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas", es importante que planee la asignación de los puntos de acceso inalámbrico y que decida con precaución qué servidor debe ser el principal y cuál el secundario. En resumen:
  
-   En un sitio con dos (o más) servidores IAS, equilibre los puntos de acceso inalámbrico en los servidores disponibles de manera que aproximadamente la mitad utilice el servidor 1 como principal y el 2 como secundario, y el resto utilice el servidor 2 como principal y el 1 como secundario.
  
-   En los sitios donde tenga únicamente un servidor IAS, éste debe ser siempre el servidor principal. Debe configurar un servidor remoto (en el sitio con conectividad más confiable a este sitio) como servidor secundario.
  
-   En los sitios donde no haya ningún servidor IAS, equilibre los puntos de acceso inalámbrico entre los servidores remotos utilizando el servidor con la conectividad de mayor rendimiento y menor latencia. Lo ideal es que estos servidores estén en diferentes sitios, a menos que tenga una conectividad de red de área extensa (WAN) de alto rendimiento.
  
La siguiente tabla muestra la configuración que debe establecer en los puntos de acceso inalámbrico. Aunque el nombre y la descripción de la configuración puede variar de un proveedor a otro, la documentación de estos puntos de acceso le ayudará a determinar los que corresponden a los elementos de la tabla.
  
**Tabla 5.3. Configuración de puntos de acceso inalámbrico**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Elemento</th>
<th style="border:1px solid black;" >Configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Parámetros de autenticación</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Modo de autenticación</td>
<td style="border:1px solid black;">Autenticación 802.1X</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Reautenticación</td>
<td style="border:1px solid black;">Habilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Volver a crear claves de forma rápida/dinámica</td>
<td style="border:1px solid black;">Habilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Tiempo de espera de actualización de claves</td>
<td style="border:1px solid black;">60 minutos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Parámetros de cifrado (esta configuración suele hacer referencia al cifrado de WEP estática)</strong></td>
<td style="border:1px solid black;">(Los parámetros de cifrado se pueden deshabilitar o sobrescribir al habilitar la opción para volver a crear claves.)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Habilitar cifrado</td>
<td style="border:1px solid black;">Habilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Denegar sin cifrado</td>
<td style="border:1px solid black;">Habilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Autenticación RADIUS</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Habilitar autenticación RADIUS</td>
<td style="border:1px solid black;">Habilitar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servidor de autenticación RADIUS principal</td>
<td style="border:1px solid black;">Dirección IP de IAS principal</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Puerto de servidor RADIUS principal</td>
<td style="border:1px solid black;">1812 (predeterminado)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servidor de autenticación RADIUS secundario</td>
<td style="border:1px solid black;">Dirección IP de IAS secundario</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Puerto de servidor RADIUS secundario</td>
<td style="border:1px solid black;">1812 (predeterminado)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Secreto compartido de autenticación RADIUS</td>
<td style="border:1px solid black;"><strong>XXXXXX</strong> (sustituir por el secreto creado)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Límite de reintentos</td>
<td style="border:1px solid black;">5</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Tiempo de espera de reintentos</td>
<td style="border:1px solid black;">5 segundos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Administración de cuentas RADIUS</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Habilitar administración de cuentas RADIUS</td>
<td style="border:1px solid black;">Habilitar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servidor de cuentas RADIUS principal</td>
<td style="border:1px solid black;">Dirección IP de IAS principal</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Puerto de servidor RADIUS principal</td>
<td style="border:1px solid black;">1813 (predeterminado)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servidor de cuentas RADIUS secundario</td>
<td style="border:1px solid black;">Dirección IP de IAS secundario</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Puerto de servidor RADIUS secundario</td>
<td style="border:1px solid black;">1813 (predeterminado)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Secreto compartido de cuentas RADIUS</td>
<td style="border:1px solid black;"><strong>XXXXXX</strong> (sustituir por el secreto creado)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Límite de reintentos</td>
<td style="border:1px solid black;">5</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Tiempo de espera de reintentos</td>
<td style="border:1px solid black;">5 segundos</td>
</tr>
</tbody>
</table>
  
**Importante:** el valor **Tiempo de espera de actualización de claves** está establecido en 60 minutos para su uso con WEP dinámica. El valor **Tiempo de espera de sesión** establecido en la directiva de acceso remoto es igual o inferior a éste. Para obtener más información, consulte la sección anterior "Modificación de la configuración del perfil de la directiva de acceso a WLAN". El valor que sea inferior tendrá preferencia, por lo que sólo deberá modificarlo en IAS. Si está utilizando WPA, debe aumentar este valor a ocho horas en el punto de acceso. Consulte la documentación del proveedor para obtener más información.
  
Utilice los mismos secretos de RADIUS creados en el procedimiento de "Adición de un cliente RADIUS al servidor IAS principal" para agregar puntos de acceso inalámbrico a IAS. Aunque puede que aún no haya configurado un servidor IAS secundario como copia de seguridad del principal, todavía podrá agregar la dirección IP del servidor al punto de acceso inalámbrico (para no tener que volver a configurarlo más adelante). La configuración de servidores IAS adicionales se explica en una sección posterior de este capítulo.
  
Según el modelo de hardware del punto de acceso inalámbrico, quizás no tenga entradas configurables independientes para los servidores de autenticación y cuentas RADIUS. Si, por el contrario, las tiene, establézcalas en el mismo servidor a menos que tenga un motivo para no hacerlo.
  
Los valores de límite y tiempo de espera de reintentos de RADIUS proporcionados en la tabla son unos valores predeterminados comunes, pero no son obligatorios.
  
**Nota:** si actualmente está utilizando puntos de acceso inalámbrico sin ninguna seguridad habilitada o sólo con WEP dinámica, deberá planear la migración a una WLAN basada en 802.1X. Para obtener más información sobre la migración desde una red inalámbrica existente, consulte la sección "Migración desde una WLAN existente" del capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas".
  
##### Configuración adicional para proteger los puntos de acceso inalámbrico
  
Además de habilitar los parámetros 802.1X, debe configurar también los puntos de acceso inalámbrico con el nivel de seguridad más alto. La mayoría del hardware de red se proporciona con unos protocolos de administración habilitados que no son seguros y con unas contraseñas de administrador establecidas en unos valores predeterminados conocidos, lo que conlleva un riesgo de seguridad. Debe establecer la configuración según la siguiente tabla; sin embargo, esta lista no es exhaustiva. Debe consultar la documentación del proveedor para obtener una información autoritativa sobre este tema. Cuando elija las contraseñas y los nombres de comunidad para el protocolo simple de administración de redes (SNMP), utilice valores complejos que incluyan letras en mayúsculas y minúsculas, números y signos de puntuación. Evite elegir caracteres que se puedan averiguar con facilidad a partir de información como el nombre de dominio, el nombre de la empresa y la dirección del sitio.
  
**Tabla 5.4. Configuración de seguridad de puntos de acceso inalámbrico**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Elemento</th>
<th style="border:1px solid black;" >Valor de configuración recomendado</th>
<th style="border:1px solid black;" >Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>General</strong></td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Contraseña de administrador</td>
<td style="border:1px solid black;">XXXXXX</td>
<td style="border:1px solid black;">Establecer una contraseña compleja.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Otras contraseñas de administración</td>
<td style="border:1px solid black;">XXXXXX</td>
<td style="border:1px solid black;">Algunos dispositivos utilizan varias contraseñas de administración para mejorar la protección del acceso mediante diversos protocolos de administración. Asegúrese de que se modifican todos los valores predeterminados para que sean más seguros.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Protocolos de administración</strong></td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Serial Console</td>
<td style="border:1px solid black;">Habilitar</td>
<td style="border:1px solid black;">Si no hay ningún protocolo cifrado disponible, este método es el más seguro para configurar puntos de acceso inalámbrico, aunque requiere conexiones físicas por cable serie entre los puntos de acceso y el terminal, por lo que no se pueden utilizar de forma remota.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Telnet</td>
<td style="border:1px solid black;">Deshabilitar</td>
<td style="border:1px solid black;">Todas las transmisiones de Telnet se realizan en texto sin formato, por lo que las contraseñas y los secretos de clientes RADIUS estarán visibles en la red. Si el tráfico de Telnet se puede asegurar mediante la seguridad de protocolos de Internet (IPSec) o SSH, podrá habilitar este servicio y usarlo de forma segura.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">HTTP</td>
<td style="border:1px solid black;">Deshabilitar</td>
<td style="border:1px solid black;">La administración HTTP suele estar en texto sin formato y padece de las mismas debilidades que Telnet sin cifrar. Se recomienda HTTPS, si está disponible.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">HTTPS (SSL o TLS)</td>
<td style="border:1px solid black;">Habilitar</td>
<td style="border:1px solid black;">Siga las instrucciones del proveedor para configurar las claves y los certificados que se necesitan.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Comunidades SNMP</strong></td>
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">SNMP es el protocolo predeterminado para la administración de redes. Utilice SNMP v3 con protección por contraseña para obtener el nivel más alto de seguridad. Éste suele ser el protocolo utilizado por las herramientas de configuración de GUI y los sistemas de administración de redes. Sin embargo, puede deshabilitarlo si no lo utiliza.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Nombre de comunidad 1</td>
<td style="border:1px solid black;">XXXXXX</td>
<td style="border:1px solid black;">El valor predeterminado suele ser &quot;pública&quot;. Cámbielo a un valor complejo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Nombre de comunidad 2</td>
<td style="border:1px solid black;">Deshabilitado</td>
<td style="border:1px solid black;">Todos los nombres de comunidad que no sean necesarios deben estar deshabilitados o establecidos en valores complejos.</td>
</tr>
</tbody>
</table>
  
No debe deshabilitar la difusión de SSID (nombre de red WLAN), ya que podría interferir en la capacidad de Windows XP para conectar con la red adecuada. Aunque se suele recomendar deshabilitar la difusión de SSID como medida de seguridad, el nivel de seguridad que proporciona no es muy alto si se utiliza un método de autenticación segura 802.1X. Incluso si la difusión de SSID desde el punto de acceso está deshabilitada, es relativamente fácil para un atacante determinar el SSID capturando paquetes de conexiones del cliente. Si le preocupa que se difunda la existencia de la WLAN, puede utilizar un nombre genérico para el SSID, el cual no será atribuible a la organización.
  
#### Replicación de la configuración de clientes RADIUS en otros servidores IAS
  
Por lo general, los puntos de acceso inalámbrico de un determinado sitio son atendidos por un servidor IAS de ese sitio. Por ejemplo, el servidor IAS del sitio A atiende a los puntos de acceso inalámbrico del sitio A, mientras que el servidor del sitio B atiende a los puntos de acceso inalámbrico del sito B, y así sucesivamente. Sin embargo, otra configuración del servidor, como las directivas de acceso remoto, será común a muchos servidores IAS. Por este motivo, la exportación e importación de información de clientes RADIUS se gestiona por separado en los procedimientos descritos en esta sección.
  
Aunque encontrará relativamente pocos casos donde la replicación de información de clientes RADIUS sea relevante, este proceso resulta útil en determinadas circunstancias (por ejemplo, cuando se tienen dos servidores IAS en el mismo sitio, funcionando como servidores RADIUS principal y secundario para todos los puntos de acceso inalámbrico de dicho sitio).
  
**Para exportar la configuración de clientes RADIUS a un archivo**
  
1.  Inicie sesión en el servidor IAS de origen y abra un shell de comandos utilizando el acceso directo **MSS WLAN Tools**.
  
2.  Si es necesario, identifique una carpeta para almacenar el archivo de salida o inserte un disco formateado vacío en la unidad del servidor.
  
3.  Ejecute el siguiente comando para exportar la configuración de clientes RADIUS:
  
    **MSSTools ExportIASClients** \[**/path:***CarpetaSalida*\]
  
    *CarpetaSalida* es un parámetro opcional utilizado para especificar la carpeta en la que se escribirá el archivo de salida. Si no se proporciona este parámetro, el archivo de salida se escribirá en el directorio actual. Si, por el contrario, sí se proporciona, la carpeta indicada debe existir.
  
4.  La secuencia de comandos crea el archivo IAS\_Clients.txt.
  
    **Precaución:** debe eliminar este archivo del servidor y almacenarlo en un lugar seguro, ya que contiene los secretos de RADIUS para todos los puntos de acceso inalámbrico configurados en el servidor. Después de exportar la configuración de clientes RADIUS, puede importarlas en los demás servidores. Lo hará normalmente para crear un servidor secundario para un determinado conjunto de puntos de acceso inalámbrico.
  
**Para importar la configuración de clientes RADIUS desde un archivo:**
  
1.  Inicie sesión en el servidor IAS de destino y abra un shell de comandos mediante el acceso directo **MSS WLAN Tools**.
  
2.  Identifique la carpeta (o el disco) donde se ha almacenado el archivo IAS\_Clients.txt con los secretos de RADIUS exportados.
  
3.  Ejecute el siguiente comando para importar la configuración de clientes RADIUS:
  
    **MSSTools ImportIASClients** \[**/path:***CarpetaEntrada*\]
  
    *CarpetaEntrada* es un parámetro opcional utilizado para especificar la carpeta desde la que se leerá el archivo. Si se especifica, esta carpeta debe existir. Si no se especifica ninguna carpeta, los archivos deberán encontrarse en el directorio actual.
  
    **Advertencia:** si ha copiado el archivo IAS\_Clients.txt en el servidor de destino, debe eliminarlo del mismo y almacenarlo en un lugar seguro, ya que contiene los secretos de RADIUS para todos los puntos de acceso inalámbrico configurados en este servidor.
  
    La importación de información de clientes RADIUS no es un proceso adicional. La configuración del cliente RADIUS importada sobrescribirá cualquier entrada de cliente existente que tenga en el servidor.
  
Puede crear un método más flexible para importar clientes RADIUS utilizando la herramienta AddRADIUSClient.exe que se proporciona con esta solución. De este modo, podrá convertir en secuencias de comandos la adición selectiva de clientes RADIUS a distintos servidores.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo se han proporcionado instrucciones sobre los siguientes temas:
  
-   Instalación y configuración del servidor IAS principal.
  
-   Instalación de servidores IAS adicionales y replicación en ellos de la configuración del servidor principal.
  
-   Adición de puntos de acceso inalámbrico a IAS como clientes RADIUS.
  
-   Configuración de puntos de acceso inalámbrico para que utilicen servidores IAS y modificación de la configuración predeterminada para mejorar la seguridad.
  
Ahora ya está preparado para configurar sus propios clientes WLAN. Puede encontrar la información necesaria para ello en el capítulo 6, "Configuración de clientes de LAN inalámbricas".
  
Debe leer el capítulo 8, "Mantenimiento de soluciones de seguridad en LAN inalámbricas". Este capítulo contiene información fundamental para mantener el funcionamiento seguro y confiable de la infraestructura de RADIUS.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Referencias
  
Esta sección ofrece referencias a otra información complementaria importante u otro material informativo de relevancia para el contenido de este capítulo.
  
-   La sección sobre el "Servicio de autenticación de Internet" de la documentación del producto Windows Server 2003 se encuentra en la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/standard/sag\_IAStopnode.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/standard/sag_iastopnode.mspx)
  
-   Para obtener más información sobre la implementación de IAS, consulte el capítulo sobre implementación de IAS del *Kit de distribución de Microsoft Windows Server 2003* en la siguiente dirección URL:
  
    [http://go.microsoft.com/fwlink/?LinkId=4716](http://go.microsoft.com/fwlink/?linkid=4716)
  
-   Para obtener más información sobre la programación de IAS utilizando la interfaz Objetos de datos de servidor, consulte la página sobre Objetos de datos de servidor en MSDN en la siguiente dirección URL:
  
    [http://msdn.microsoft.com/library/en-us/sdo/sdo/server\_data\_objects\_.asp](http://msdn.microsoft.com/es-es/library/ms717286.aspx)
  
-   Para obtener más información sobre el registro IAS y RADIUS, consulte la sección sobre el registro de acceso remoto de la documentación del producto IAS en la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/standard/sag\_ias\_log\_conc.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/standard/sag_ias_log_conc.mspx)
  
-   Para obtener más información sobre la compatibilidad de Pocket PC para la reconexión rápida de PEAP, consulte el artículo 827824, "FIX: Wireless Clients Cannot Connect When the PEAP Fast Reconnect Authentication Option is Turned On" de Microsoft Knowledge Base en la siguiente dirección URL:
  
    <http://support.microsoft.com/default.aspx?scid=kb;en-us;827824>
  
-   Para obtener más información sobre la configuración de la compatibilidad de RADIUS específica para los puntos de acceso, consulte la página sobre los atributos específicos del proveedor de la documentación del producto IAS en la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/standard/sag\_ias\_attributes\_conc\_top.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/standard/sag_ias_attributes_conc_top.mspx)
  
-   Para obtener más información sobre la implementación de una WLAN, consulte el capítulo sobre la implementación de una LAN inalámbrica del *Kit de distribución de Microsoft Windows Server 2003* en la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/deployguide/DNSBM\_WIR\_OVERVIEW.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/deployguide/dnsbm_wir_overview.mspx)
  
-   Para obtener más información sobre la tecnología inalámbrica de Windows XP, consulte las notas del producto *Windows XP Wireless Deployment Technology and Component Overview* en la siguiente dirección URL:
  
    [http://www.microsoft.com/windowsxp/pro/techinfo/administration/  
    networking/default.asp](http://www.microsoft.com/windowsxp/pro/techinfo/administration/networking/default.asp)
  
(Este artículo contiene referencias a guías de otros productos y vínculos a sitios Web que sólo están disponibles en inglés.)
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 6: Configuración de clientes de LAN inalámbricas
  
[](#eiaac)[Información general](#eiaac)  
[](#ehaac)[Requisitos previos del capítulo](#ehaac)  
[](#egaac)[Preparación de la implementación](#egaac)  
[](#efaac)[Acceso de los usuarios y los equipos a la WLAN](#efaac)  
[](#eeaac)[Configuración de clientes WLAN en Windows XP](#eeaac)  
[](#edaac)[Configuración de clientes Pocket PC 2003](#edaac)  
[](#ecaac)[Resumen](#ecaac)  
[](#ebaac)[Referencias](#ebaac)
  
### Información general
  
En este capítulo se proporciona información sobre la implementación y la configuración de red de los clientes de la red de área local inalámbrica (WLAN) y la conexión de los clientes a la WLAN. Se incluyen los procedimientos para conectar clientes Microsoft® Windows® XP (Professional y Tablet Edition) y Pocket PC 2003 a la WLAN.
  
En el capítulo también se proporcionan detalles sobre la comprobación de la pertenencia al grupo de seguridad de los usuarios y equipos de la WLAN, la configuración de la WLAN utilizando la directiva de grupo de los clientes Windows XP y los procedimientos para configurar clientes Pocket PC.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Requisitos previos del capítulo
  
Además de los requisitos previos que se describen en el capítulo 3, "Preparación del entorno", debe estar familiarizado con los siguientes temas:
  
-   Configuración de Windows XP e instalación de controladores.
  
-   Configuración y uso de Pocket PC 2003.
  
Debe leer e implementar la información que se proporciona en el capítulo 3, "Preparación del entorno", el capítulo 4, "Creación de la entidad emisora de certificados de red" y el capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas". Asimismo, se recomienda leer también la información sobre el diseño y el planeamiento que se incluye en el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas" y entender la arquitectura y el diseño de la solución.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Preparación de la implementación
  
Para realizar los procedimientos de configuración de directivas de grupo de este capítulo, debe iniciar la sesión con una cuenta que sea miembro del grupo Admins. del dominio para el dominio en el que se instala la configuración de WLAN. De forma predeterminada, la cuenta de administrador integrada del dominio pertenece a este grupo, aunque puede utilizar cualquier otra cuenta que pertenezca al grupo.
  
Para realizar los procedimientos de verificación del equipo cliente Windows XP, debe pertenecer al grupo de administradores local de ese equipo.
  
#### Herramientas necesarias
  
En la tabla siguiente se enumeran las herramientas necesarias para implementar los procedimientos de este capítulo.
  
**Tabla 6.1. Herramientas necesarias**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Herramienta</th>
<th style="border:1px solid black;" >Descripción</th>
<th style="border:1px solid black;" >Fuente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Consola de administración de directivas de grupo</strong> (GPMC)</td>
<td style="border:1px solid black;">Herramienta de administración avanzada para importar y exportar grupos de directiva de grupo.</td>
<td style="border:1px solid black;">Los pasos de instalación se incluyen en el capítulo 3, &quot;Preparación del entorno&quot;.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Usuarios y equipos de Active Directory</strong></td>
<td style="border:1px solid black;">Herramienta Microsoft Management Console (MMC) para administrar usuarios, grupos y equipos del servicio de directorio de Microsoft Active Directory® y otros objetos de Active Directory.</td>
<td style="border:1px solid black;">Se instala como parte de Windows Server™ 2003.</td>
</tr>
</tbody>
</table>
  
#### Configuración de cliente WLAN
  
En la tabla siguiente se enumeran algunas de las principales configuraciones que se utilizan en este capítulo.
  
**Tabla 6.2. Configuración de cliente WLAN**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Elemento de configuración</th>
<th style="border:1px solid black;" >Valor de configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Grupo para permitir el acceso a la WLAN</td>
<td style="border:1px solid black;">Acceso a LAN inalámbrica</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Grupo para permitir el acceso a la WLAN de los usuarios</td>
<td style="border:1px solid black;">Usuarios de LAN inalámbrica</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Grupo para permitir el acceso a la WLAN de los equipos</td>
<td style="border:1px solid black;">Equipos de LAN inalámbrica</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Nombre de objeto de directiva de grupo de WLAN</td>
<td style="border:1px solid black;">Configuración de cliente WLAN</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Grupo de seguridad de filtrado de objetos de directiva de grupo</td>
<td style="border:1px solid black;">Configuración del equipo de LAN inalámbrica</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Nombre de directiva de red inalámbrica</td>
<td style="border:1px solid black;">Configuración de cliente WLAN de Windows XP (Protocolo de autenticación extensible protegido (PEAP)-Privacidad equivalente por cable (WEP))</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Nombre de red de WLAN (SSID)</td>
<td style="border:1px solid black;"><em>LucerneWLAN</em> (cambie este valor por el identificador del conjunto de servicios (SSID) de la WLAN)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Tipo de Protocolo de autenticación extensible (EAP)</td>
<td style="border:1px solid black;">PEAP</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Método de autenticación de PEAP</td>
<td style="border:1px solid black;">Contraseña protegida (EAP-MSCHAP v2)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Reconexión rápida de PEAP</td>
<td style="border:1px solid black;">Habilitado</td>
</tr>
</tbody>
</table>
  
Los valores que aparecen en cursiva se tienen que sustituir por los valores relativos a su entorno.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Acceso de los usuarios y los equipos a la WLAN
  
Para controlar el acceso de los usuarios y los equipos a un servidor de acceso a red (por ejemplo, a un punto de acceso inalámbrico), establezca el permiso de acceso telefónico en la cuenta de dominio del usuario o el equipo. Éste era el método que utilizaba Windows NT® 4.0 para controlar el acceso de usuarios al servicio de acceso remoto (RAS). No obstante, con este método, el control del acceso a la red de un gran número de usuarios se complica bastante. Además, se trata de un valor de configuración de "todo o nada ", es decir, que no puede permitir el acceso a una red privada virtual (VPN) y bloquear al mismo tiempo el acceso a la WLAN de un usuario determinado.
  
El Servicio de autenticación de Internet (IAS), con Windows 2000 y Windows Server 2003, permite controlar el acceso a los servicios de red utilizando los grupos de seguridad de Active Directory asociados con una directiva de acceso remoto. Este método es más flexible y mucho más fácil de gestionar, ya que permite utilizar las pertenencias a grupos para controlar el acceso a un servicio de red.
  
#### Control del acceso a la WLAN utilizando grupos de seguridad
  
La directiva de acceso remoto (RAP) de IAS controla el acceso a la WLAN. La RAP de esta solución se ha configurado en el capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas". Esta directiva incluye un filtro para que sólo puedan tener acceso a la WLAN los miembros del grupo de seguridad Acceso a LAN inalámbrica.
  
El grupo Acceso a LAN inalámbrica no se rellena directamente con cuentas de usuario y de equipo. Tiene como miembros a dos grupos de seguridad: Usuarios de LAN inalámbrica y Equipos de LAN inalámbrica. La solución convierte en miembros de estos grupos a los usuarios del domino y a los equipos del dominio, respectivamente, lo que permite a todos los usuarios y equipos conectarse a la WLAN de forma predeterminada. Puede encontrar más información sobre este tema en la sección "Modelo de administración de usuario y equipo de WLAN" del capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas".
  
##### Utilización de grupos de seguridad para realizar un control más específico
  
Permitir a todos los usuarios y equipos tener acceso a la WLAN es un modelo de administración muy sencillo, pero puede que tenga que realizar un control más específico sobre qué usuarios y equipos pueden tener acceso a la WLAN. Para ello, elimine usuarios del dominio y equipos del dominio de Usuarios de LAN inalámbrica y Equipos de LAN inalámbrica, respectivamente. A continuación, puede agregar los usuarios y los equipos específicos a los que desee otorgar acceso como miembros de estos grupos.
  
No agregue directamente usuarios y grupos al grupo Acceso a LAN inalámbrica, ya que es un grupo universal y, por lo tanto, sus miembros se publican en el catálogo global de bosque. La publicación en el catálogo local implica que los cambios de pertenencia se replicarán en todos los controladores de dominio de la organización. Al agregar usuarios y grupos a los grupos específicos de dominio (Usuarios de LAN inalámbrica y Equipos de LAN inalámbrica), los cambios de replicación se limitan a los controladores de dominio con un solo dominio.
  
**Nota:** los Pocket PC no tienen cuentas de equipo de Active Directory, por lo que no es necesario agregarlos al grupo Equipos de LAN inalámbrica. Sólo utilizan la cuenta de usuario para autenticarse en la WLAN, por lo que sólo es relevante la cuenta del usuario de Pocket PC.
  
Los usuarios sólo reciben información modificada sobre la pertenencia al grupo al iniciar la sesión. Por lo tanto, los usuarios deberán cerrar la sesión y volverla a iniciar después de crear y rellenar los grupos de acceso a la WLAN. De la misma forma, los equipos cliente también se deben reiniciar después de realizar cambios de pertenencia a grupos.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de clientes WLAN en Windows XP
  
En esta sección se describen los procedimientos para establecer la configuración del cliente WLAN en Windows XP. Estos procedimientos permiten configurar la autenticación de contraseña PEAP utilizando la privacidad equivalente por cable (WEP) con clave dinámica en la protección de los datos. La configuración se puede aplicar a Windows XP Professional y Windows XP Tablet Editions.
  
Para obtener instrucciones sobre la configuración de la administración de claves y la protección de datos de acceso inalámbrico protegido (WPA), consulte el Apéndice B, "Uso de WPA en la solución".
  
#### Instalación de las revisiones y actualizaciones necesarias
  
Asegúrese de que se hayan aplicado todas las revisiones y actualizaciones necesarias a los equipos cliente, por ejemplo:
  
-   Las revisiones críticas de seguridad.
  
-   Los Service Packs de Windows XP (Service Pack 1 o posterior).
  
-   El cliente WPA de Windows XP (si es necesario).
  
-   Las revisiones de Windows relacionadas con WLAN, como Wireless Update Rollup Package para Windows XP (consulte el artículo 826942 de Knowledge Base). Este paquete es el recomendado a menos que esté instalado Windows XP SP2.
  
-   Los controladores actualizados de WLAN del adaptador de red o el proveedor del equipo.
  
#### Creación de objetos de directiva de grupo de la configuración de WLAN
  
Para automatizar la entrega de la configuración del cliente WLAN, utilice la directiva de grupo de Active Directory. El editor de directivas de grupo en Windows Server 2003 incluye un grupo de configuraciones denominado Directiva de red inalámbrica, que permite establecer configuraciones de cliente específicos de la WLAN.
  
**Importante:** se supone que los equipos cliente están unidos al dominio y que pueden conectarse a una LAN con cable para recibir la configuración de cliente WLAN.
  
Puede crear objetos de directiva de grupo utilizando GPMC o **Usuarios y equipos de Active Directory**.
  
**Importante:** la configuración del objeto de directiva de grupo de directiva de red inalámbrica no aparecerá en el editor del objeto de directiva de grupo si lo edita desde un sistema Windows 2000 o Windows XP. Debe modificar esta configuración desde un sistema Windows Server 2003 o un sistema con las herramientas de administración de Windows Server 2003 instaladas. No obstante, la configuración funciona con los controladores de dominio de Windows 2000 y Windows Server 2003. Esta configuración no existe en el objeto de directiva local de ninguna versión de Windows.
  
**Para crear un objeto de directiva de grupo de cliente WLAN utilizando GPMC**
  
1.  Abra la GPMC y seleccione el objeto de dominio del dominio que esté configurando.
  
2.  Haga clic con el botón secundario en el dominio y seleccione **Crear y vincular aquí un GPO**.
  
    **Nota:** el objeto de directiva de grupo está vinculado en el nivel del dominio; por lo tanto, la configuración estará disponible en todos los equipos del dominio. Si lo prefiere, puede restringir el ámbito del objeto de directiva de grupo vinculándolo con una unidad organizativa (OU) de nivel inferior.
  
3.  Cuando se le solicite el nombre, escriba **Configuración de cliente WLAN**.
  
4.  En el panel derecho, haga doble clic en el objeto de directiva de grupo **Configuración de cliente WLAN** que acaba de crear. En el panel derecho aparecen ahora las propiedades del objeto de directiva de grupo.
  
5.  Haga clic en la ficha **Ámbito**. En la lista **Filtrado de seguridad**, seleccione **Usuarios autenticados** y elimínelo utilizando el botón **Quitar**.
  
6.  Haga clic en **Agregar** para agregar otro grupo.
  
7.  Escriba (o explore hasta encontrar) **Configuración del equipo de LAN inalámbrica**.
  
    **Nota:** la pertenencia eficaz del grupo Configuración del equipo de LAN inalámbrica es el grupo Equipos del dominio. Este grupo es miembro de Equipos de LAN inalámbrica, que a su vez es miembro del grupo Configuración del equipo de LAN inalámbrica. El objeto de directiva de grupo en el nivel del dominio (consulte el paso 1) permite a todos los equipos del dominio recibir la configuración de cliente WLAN. Si desea restringir la configuración a un subconjunto menor, elimine Equipos del dominio de la pertenencia del grupo Equipos de LAN inalámbrica.
  
8.  Haga clic en la ficha **Detalles** y seleccione **Parámetros de configuración de usuario deshabilitados** en la lista desplegable **Estado de GPO**. Haga clic en **Aceptar** para confirmar la operación.
  
9.  Haga clic con el botón secundario en el panel izquierdo y seleccione **Editar** para editar la configuración del objeto de directiva de grupo.
  
10. Cuando se abra el editor del objeto de directiva de grupo, desplácese hasta **\\Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de red inalámbrica (IEEE 802.11)**.
  
11. Seleccione el objeto **Directivas de red inalámbrica (IEEE 802.11)** en el panel de exploración y, a continuación, seleccione **Crear directiva de red inalámbrica** en el menú **Acción**.
  
12. Utilice el asistente para llamar a la directiva **Configuración de cliente WLAN de Windows XP (PEAP-WEP)**. Deje seleccionada la casilla de verificación **Modificar propiedades** y, a continuación, haga clic en **Finalizar** para cerrar el asistente.
  
13. Haga clic en la ficha **Redes preferidas** y, a continuación, haga clic en **Agregar** para agregar una nueva red preferida.
  
14. En el campo **Nombre de red (SSID)**, escriba el nombre de la red inalámbrica.
  
15. En el campo **Descripción**, escriba una descripción de la red.
  
    **Nota:** si ya tiene configurada una WLAN y desea ejecutarla en paralelo con la WLAN basada en 802.1X de esta solución, debe utilizar un SSID para la nueva WLAN.
  
16. Haga clic en la ficha **IEEE 802.1x** y seleccione **EAP protegido (PEAP)** en la lista desplegable **Tipo de EAP**.
  
17. Haga clic en el botón **Configuración** para modificar la configuración PEAP. En la lista **Entidades emisoras raíz confiables**, seleccione el certificado de entidad emisora raíz de la entidad emisora que haya instalado en el capítulo 4, "Creación de la entidad emisora de certificados de red".
  
    **Importante:** si necesita instalar de nuevo la entidad emisora desde cero (no sólo restaurarla desde la copia de seguridad), modifique el objeto de directiva de grupo y seleccione el certificado de entidad emisora raíz de la nueva entidad emisora.
  
18. Seleccione **Contraseña protegida (EAP-MSCHAP v2)** en **Seleccione el método de autenticación** y seleccione la opción **Habilitar reconexión rápida**.
  
19. Cierre cada una de las ventanas de propiedades haciendo clic en **Aceptar**.
  
20. Cierre el editor del objeto de directiva de grupo y la GPMC.
  
Para crear el objeto de directiva de grupo utilizando **Usuarios y equipos de Active Directory** (si no ha instalado la GPMC), realice los siguientes pasos en lugar de los pasos del 1 al 10 del procedimiento anterior.
  
**Para crear un objeto de directiva de grupo utilizando Usuarios y equipos de Active Directory**
  
1.  Abra **Usuarios y equipos de Active Directory** y seleccione el objeto de dominio.
  
2.  Haga clic con el botón secundario en el objeto de domino y seleccione **Propiedades**.
  
3.  Haga clic en la ficha **Directiva de grupo** y, a continuación, en el botón **Nueva**.
  
4.  Escriba **Configuración de cliente WLAN** como nombre de objeto de directiva de grupo.
  
5.  Haga clic en el botón **Propiedades** y, a continuación, en la ficha **Seguridad**.
  
6.  Seleccione **Usuarios autenticados** en la lista **Nombres de grupos o usuarios** y haga clic en el botón **Quitar**.
  
7.  Haga clic en **Agregar** y escriba (o explore hasta encontrar) **Configuración del equipo de LAN inalámbrica**. Haga clic en **Aceptar**.
  
8.  Con el nombre del grupo **Configuración del equipo de LAN inalámbrica** resaltado en la lista **Nombres de grupos o usuarios**, haga clic en los permisos de **Lectura** y **Aplicar directiva de grupo** en la columna **Permitir** de la lista **Permisos**.
  
9.  Haga clic en la ficha **General** y en **Deshabilitar los parámetros de configuración de usuario**. Haga clic en **Sí** si aparecen mensajes de advertencia.
  
10. Haga clic en **Aceptar** para aplicar los cambios y cerrar la ventana de propiedades del objeto de directiva de grupo.
  
11. Haga clic en el botón **Modificar** para modificar la directiva y desplácese hasta **\\Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de red inalámbrica (IEEE 802.11)**.
  
12. Repita los pasos del 11 al 20 del procedimiento anterior.
  
#### Implementación de la configuración de WLAN
  
Si realiza la migración de una WLAN existente (WEP estática no protegida o de otro tipo), deberá implementar la configuración de la directiva de grupo de WLAN de la nueva red basada en 802.1X durante varios días, o incluso semanas, antes de establecer la configuración de 802.1X en los puntos de acceso inalámbrico y activar la nueva WLAN. De esta forma, los equipos cliente tendrán una amplia oportunidad de descargar y aplicar la directiva de grupo **Configuración de cliente WLAN**, aunque sólo se conecten con la configuración de la LAN con cable de manera ocasional.
  
También puede aplicar la configuración de directiva de grupo en los equipos cliente antes de que Windows instale y configure un adaptador de red de WLAN. La configuración de WLAN se omitirá hasta que se instale un adaptador de red de WLAN. Cuando se instale el adaptador de red, se configurará automáticamente con la configuración de la directiva de grupo de WLAN.
  
#### Comprobación de la aplicación de la Directiva de grupo de WLAN
  
Para comprobar la aplicación correcta de la configuración de objetos de directiva de grupo de la WLAN, debe iniciar una sesión en un equipo cliente. El grupo Equipos del dominio es miembro del grupo de seguridad Configuración del equipo de LAN inalámbrica, que se utiliza para filtrar qué equipos reciben la configuración de WLAN en el objeto de directiva de grupo Configuración de cliente WLAN. Por lo tanto, todos los equipos del dominio deben haber recibido esta configuración del objeto de directiva de grupo. Puede que tenga que reiniciar el equipo si no se ha reiniciado desde la creación del grupo Configuración del equipo de LAN inalámbrica.
  
**Nota:** tiene que tener instalado un adaptador de red de WLAN en el equipo para poder ver la configuración de red inalámbrica.
  
**Para comprobar la implementación correcta de la configuración de WLAN**
  
1.  Inicie una sesión como miembro del grupo de administradores local en un equipo cliente.
  
2.  Haga doble clic en la carpeta **Conexiones de red** en el **Panel de control**.
  
3.  Vea las propiedades del icono de **Conexión de red inalámbrica** correspondiente a la tarjeta inalámbrica. En la ficha **Redes inalámbricas**, verá el nuevo SSID (nombre) de red inalámbrica en **Redes preferidas**.
  
4.  Seleccione el nuevo SSID de red inalámbrica y haga clic en **Propiedades** para ver las propiedades y comprobar que coincidan con las seleccionadas en la Directiva de grupo de WLAN.
  
5.  Si el SSID no aparece en **Redes preferidas** o la configuración de la red que aparece para este SSID no coincide con la de la Directiva de grupo de WLAN, cierre todos los cuadros de diálogo de redes inalámbricas y ejecute el siguiente comando desde el símbolo del sistema.
  
    **Gpupdate /force**
  
    Después de un par de minutos, vuelva a comprobar la configuración. Si la configuración continúa sin aparecer, consulte la sección "Solución de problemas" en el capítulo 8, "Mantenimiento de soluciones de seguridad en LAN inalámbricas".
  
#### Comprobación del certificado de entidad emisora raíz en el cliente
  
Para autenticarse en el servidor IAS utilizando PEAP, los clientes deben tener el certificado de la entidad emisora de red (que se instala mediante las instrucciones del capítulo 4, "Creación de la entidad emisora de certificados de red") en el almacenamiento de la entidad emisora raíz de confianza. Este certificado se ha publicado en Active Directory como parte de la instalación de la entidad emisora. Todos los miembros del bosque de Active Directory descargarán e instalarán automáticamente este certificado en el almacenamiento de la entidad emisora raíz de confianza.
  
**Para comprobar que el certificado de entidad emisora raíz se ha instalado**
  
1.  Inicie la sesión en el equipo cliente como Administrador.
  
2.  Ejecute MMC.exe (desde la opción de menú **Inicio, Ejecutar** o desde un shell de comandos).
  
3.  Desde el menú **Archivo** de MMC, seleccione **Agregar o quitar complemento**.
  
4.  En la ventana **Agregar o quitar complemento**, haga clic en el botón **Agregar**. Seleccione el elemento **Certificados** en la lista de complementos disponibles.
  
5.  Seleccione **Cuenta de equipo** y, a continuación, haga clic en **Siguiente**.
  
6.  Haga clic en **Finalizar**.
  
7.  Cierre las ventanas **Agregar un complemento independiente** y **Agregar o quitar complemento**.
  
8.  En el panel izquierdo, desplácese hasta Certificados (equipo local)\\Entidades emisoras raíz confiables\\Certificados.
  
9.  Busque el certificado de la entidad emisora, que aparecerá con el nombre que se le proporcionó durante la instalación de la entidad emisora.
  
10. Si el certificado no aparece en la lista, abra un shell de comandos y escriba el comando:
  
    **Gpupdate /force**
  
11. Vuelva a la consola de administración de **Certificados**. Haga clic con el botón secundario en el nodo **Certificados (equipo local)**, seleccione **Actualizar** y vuelva a comprobar si aparece el certificado de entidad emisora.
  
    Si el certificado continúa sin aparecer, consulte la sección "Solución de problemas" en el capítulo 8, "Mantenimiento de soluciones de seguridad en LAN inalámbricas".
  
#### Comprobación de la conexión con la WLAN
  
Si ha comprobado la configuración de objetos de directiva de grupo de la WLAN y el certificado de entidad emisora raíz, ahora ya puede probar la conexión con la WLAN utilizando un equipo cliente.
  
**Para probar la conexión con la WLAN**
  
1.  Inicie una sesión como usuario del dominio con acceso autorizado a la WLAN en un equipo cliente que tenga una tarjeta de WLAN instalada y que no esté conectado a la red con cable. De forma predeterminada, todos los usuarios del dominio tienen acceso a la WLAN.
  
    **Nota:** si la WLAN no funciona en este punto y el usuario no tiene credenciales en caché en el equipo, el inicio de sesión fallará.
  
2.  Desde el símbolo del sistema, utilice el comando **ping** para comprobar la conexión a través de la red con otro equipo de la misma.
  
    Si el comando **ping** (o el inicio de sesión) falla, consulte la subsección sobre supervisión de la conexión del cliente con la WLAN de la sección "Solución de problemas" en el capítulo 8, "Mantenimiento de soluciones de seguridad en LAN inalámbricas".
  
Si desea obtener más información sobre los procedimientos de prueba de los clientes WLAN, consulte el capítulo 7, "Prueba de soluciones de seguridad en LAN inalámbricas".
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración de clientes Pocket PC 2003
  
Pocket PC 2003 es totalmente compatible con las redes WLAN de 802.1X utilizando PEAP (con contraseñas) o EAP-TLS (Protocolo de autenticación extensible-Seguridad de la capa de transporte) (con certificados). No obstante, Pocket PC 2003 es un sistema operativo modular y el proveedor del dispositivo de mano puede elegir si desea incluir o no este servicio; por lo tanto, no debe asumir que todos los dispositivos Pocket PC 2003 tienen capacidad para WLAN. Los principales proveedores de estos dispositivos proporcionan sistemas con capacidad para WLAN de 802.1X, ya sea con hardware de WLAN integrado o con un adaptador de red de WLAN de complemento. En esta sección se describe la configuración de la interfaz genérica de WLAN de Pocket PC, basándose en HP IPAQ 5550 Pocket PC. No obstante, algunos proveedores implementan sus propios controladores e interfaces de WLAN. Puede que las siguientes instrucciones no sean correctas para estos últimos dispositivos, en cuyo caso debe seguir las instrucciones proporcionadas por el proveedor del dispositivo.
  
Algunos proveedores de dispositivos Pocket PC también ofrecen compatibilidad con WLAN de 802.1X en Pocket PC 2002. Pocket PC 2002 no se ha probado con esta solución. Consulte el sitio Web del proveedor para obtener más información sobre la compatibilidad con WLAN de Pocket PC 2002.
  
#### Preparación del dispositivo Pocket PC
  
Antes de configurar el dispositivo, obtenga e instale las actualizaciones pertinentes de Pocket PC que tenga disponibles el proveedor, por ejemplo:
  
-   Actualizaciones de ROM (Memoria de sólo lectura). Pueden contener una amplia variedad de actualizaciones, incluso de controladores.
  
-   Actualizaciones de controladores de red.
  
-   Otras actualizaciones de red o de WLAN que sean relevantes para la red de 802.1X.
  
    **Importante:** antes de instalar las actualizaciones, lea atentamente la documentación que se incluye con cada una de ellas. Puede que algunas actualizaciones sean incompatibles con otras o con sus objetivos. Por ejemplo, HP ha publicado una actualización de la serie IPAQ 555x para que sea compatible con Cisco LEAP, pero es incompatible con la actualización del controlador de WLAN de 802.1X, por lo que PEAP no podrá funcionar.
  
#### Disponibilidad del certificado de entidad emisora
  
Debe instalar el certificado de la entidad emisora de red en el almacenamiento de la entidad emisora raíz de confianza de todos los Pocket PC que se tengan que conectar a la WLAN. Para ello, debe exportar el certificado de entidad emisora y hacer que esté disponible para los usuarios de Pocket PC o el personal de tecnología de la información (TI).
  
**Para exportar el certificado de entidad emisora**
  
1.  Inicie una sesión en el servidor de la entidad emisora y abra un shell de comandos.
  
2.  Ejecute el siguiente comando para exportar el certificado de entidad emisora a un archivo:
  
    **certutil -ca.cert rootca.cer**
  
    Puede especificar una ruta al archivo Rootca.cer si desea guardarlo en otra carpeta. Debe cerrar la ruta y el nombre del archivo entre comillas si contiene espacios incrustados.
  
3.  Copie el archivo de certificado en un recurso compartido o un directorio de servidor Web para que los usuarios puedan descargarlo fácilmente cuando sea necesario para la instalación de Pocket PC.
  
#### Configuración de Pocket PC
  
Debe configurar cada Pocket PC con la configuración de WLAN y el certificado de entidad emisora para poder conectarlo a la WLAN. Necesitará algún medio para copiar el archivo de certificado en Pocket PC. Este procedimiento asume el uso de la conexión ActiveSync® establecida utilizando una conexión de soporte de acoplamiento, infrarrojos o Bluetooth. También puede utilizar medios extraíbles (por ejemplo, Compact Flash, Secure Digital o una tarjeta multimedia) para transferir el archivo de certificado, o utilizar una conexión de WLAN no autenticada para que Pocket PC se descargue el certificado de un sitio Web. También puede enviar el certificado al usuario por correo electrónico y permitirle que realice la sincronización (para transferir el correo electrónico a Pocket Outlook®), para que ejecute después el archivo de certificado adjunto.
  
**Para importar el certificado de entidad emisora a Pocket PC**
  
1.  Conecte Pocket PC a un equipo host utilizando ActiveSync (puede que tenga que establecer una sociedad con ActiveSync para ello) y su método de conexión preferido.
  
2.  En el equipo host, utilice la opción **Explorar** de ActiveSync para abrir una ventana de carpeta en el dispositivo; debe abrir la carpeta **Mis documentos**.
  
3.  Obtenga el archivo de certificado de entidad emisora de la ubicación donde esté publicado y cópielo en la carpeta **Mis documentos**. Puede hacer caso omiso de la advertencia sobre la conversión de archivos. Ya puede desconectar el dispositivo de la conexión de ActiveSync.
  
4.  En Pocket PC, busque el archivo de certificado de entidad emisora utilizando el **Explorador de archivos** y haga doble punteo en el archivo.
  
5.  Se le preguntará si desea instalar el certificado. Compruebe que el nombre de la entidad emisora coincide con el nombre de la entidad emisora de red y haga clic en **Sí** para instalarlo.
  
    Para comprobar si el certificado se ha instalado correctamente, seleccione **Configuración**, **Sistema**, **Certificados**, y haga clic en la ficha **Raíz**.
  
**Para establecer la configuración de WLAN de 802.1X en Pocket PC**
  
1.  Si el adaptador de WLAN no está habilitado en el dispositivo, habilítelo utilizando un conmutador de hardware o una herramienta de software.
  
2.  Si aparece un mensaje emergente indicando que se ha encontrado una red nueva, seleccione **Trabajo** como la ubicación en la que conectará la WLAN. A continuación, puntee en **Configuración**.
  
    Si el mensaje emergente no aparece (porque la WLAN se ha detectado previamente), realice los pasos siguientes:
  
    -   Puntee en el icono **Conectividad** (dos flechas apuntando en direcciones opuestas) en la barra de títulos de Pocket PC y puntee en **Configuración**.
  
    -   Puntee en la ficha **Avanzadas** y, a continuación, puntee en el botón **Tarjeta de red**.
  
        En la ficha **Inalámbrica**, debe aparecer el SSID de la WLAN en la lista de redes inalámbricas disponibles (si hay otras WLAN dentro de los límites, deberá aparecer aquí su nombre).
  
    -   Puntee en el nombre de la WLAN en la lista.
  
3.  En la ficha **General**, seleccione **Trabajo** en la lista **Conecta a:**.
  
4.  En la ficha **Autenticación**, seleccione las siguientes opciones:
  
    -   **Cifrado de datos (WEP habilitado)**
  
    -   **La clave la proporciono yo automáticamente**
  
    -   **Habilitar el acceso a la red mediante IEEE 802.1X**
  
    Desactive la opción **Autenticación de red (modo compartido)**.
  
5.  En la lista **Tipo de Protocolo de autenticación extensible:**, seleccione **PEAP**.
  
6.  Puntee en **Aceptar** para cerrar la pantalla de configuración de WLAN.
  
7.  Cuando tenga que especificar las credenciales de dominio para conectarse a la WLAN, escriba el nombre, la contraseña y el dominio de un usuario que esté autorizado para conectarse a la WLAN.
  
    **Advertencia:** sólo debe seleccionar la opción **Guardar contraseña** si se ha implementado un mecanismo de seguridad sólido para proteger el dispositivo del uso no autorizado. Por ejemplo, un mecanismo como la digitalización de huellas digitales o el acceso de contraseñas seguras. Recuerde que las credenciales de usuario se utilizan para autenticar los recursos del dominio así como la WLAN. Si están en peligro, permitirán a un intruso tener acceso a todos los recursos de red internos en la WLAN sin que se pueda detectar.
  
8.  Si ha llegado a la configuración de WLAN a través del menú emergente **Nueva red** del paso 2, puntee en el icono **Conectividad** de la barra de títulos de Pocket PC y puntee en **Configuración** para abrir la pantalla **Configuración de conexiones**.
  
9.  Puntee en la ficha **Avanzadas** y, a continuación, en el botón **Tarjeta de red**. (Ya estará en esta pantalla si no ha utilizado el menú emergente **Nueva red** del paso 2.)
  
10. En la lista **Redes inalámbricas**, aparecerá el nombre de la WLAN que acaba de configurar. El estado debería ser **Conectada**; si no es así, puntee y mantenga el lápiz en el nombre y, a continuación, puntee en **Conectar**. (Puede que tenga que volver a escribir las credenciales del usuario.)
  
11. Si la WLAN aparece ahora como **Conectada**, puntee en **Aceptar** para cerrar las pantallas **Configurar redes inalámbricas** y **Configuración de conexiones**.
  
    **Nota:** si va a proporcionar estas instrucciones a los usuarios de Pocket PC para que configuren sus propios dispositivos, pueden introducir sus credenciales de dominio cuando se les indique. No obstante, si los ingenieros de soporte técnico de TI preconfiguran los Pocket PC para los usuarios, debe proporcionarles cuentas de dominio válidas (con acceso a la WLAN); es muy importante que los *ingenieros* no seleccionen la opción **Guardar contraseña** cuando utilicen estas cuentas. De esta forma, los usuarios deberán introducir sus credenciales cuando se conecten la primera vez utilizando Pocket PC.
  
#### Comprobación de la conexión de Pocket PC a la WLAN
  
Puede comprobar que Pocket PC se ha conectado correctamente a la WLAN de varias formas. La forma más sencilla es conectarse a una aplicación de la red, por ejemplo, un sitio Web. (Puede que tenga que configurar un servidor proxy en el dispositivo si el servidor Web no está en la LAN.)
  
Si la conexión falla, consulte la sección "Solución de problemas" en el capítulo 8, "Mantenimiento de soluciones de seguridad en LAN inalámbricas".
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo se describe la configuración de red WLAN para clientes Windows XP y Pocket PC. Se proporciona información sobre el uso de grupos de seguridad para controlar el acceso a la WLAN, la configuración de directivas de grupo para implementar la configuración de WLAN en clientes Windows XP y los pasos de configuración de los clientes Pocket PC 2003.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Referencias
  
Esta sección ofrece referencias a otra información complementaria importante u otro material informativo de relevancia para el contenido de este capítulo.
  
-   Si desea obtener más información sobre la administración del acceso a la WLAN de los grupos de seguridad y los usuarios, consulte el tema introductorio a las directivas de acceso remoto de la documentación del producto Windows Server 2003, que está disponible en el siguiente URL:
  
    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/standard/sag\_rap\_intro.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/standard/sag_rap_intro.mspx)
  
-   Para obtener más información sobre Wireless Update Rollup Package para Windows XP, consulte la siguiente dirección URL:
  
    <http://support.microsoft.com/default.aspx?scid=826942>
  
-   Para obtener más información sobre la configuración de la red WLAN utilizando directivas de grupo, consulte el tema sobre la definición de directivas de red inalámbrica basadas en Active Directory de la documentación del producto Windows Server 2003, que está disponible en la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/standard/wireless\_definepolicy\_inGP\_topnode.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/standard/wireless_definepolicy_ingp_topnode.mspx)
  
-   Consulte al proveedor del dispositivo para obtener información técnica sobre la compatibilidad de WLAN en Pocket PC. Para obtener más información técnica, consulte la información general de la tecnología inalámbrica .NET de Windows CE en Microsoft Developer Network en la siguiente dirección URL:
  
    [http://msdn.microsoft.com/library/en-us/wcemain4/  
    html/cmconwindowscenetwirelesstechnologyoverview.asp](http://msdn.microsoft.com/en-us/embedded/aa714425.aspx)
  
(Este artículo contiene referencias a guías de otros productos y vínculos a sitios Web que sólo están disponibles en inglés.)
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 7: Prueba de soluciones de seguridad en LAN inalámbricas
  
[](#eeaad)[Introducción](#eeaad)  
[](#edaad)[Cómo se ha probado la solución en Microsoft](#edaad)  
[](#ecaad)[Comprobación de la implementación](#ecaad)  
[](#ebaad)[Herramientas de la prueba](#ebaad)  
[](#eaaad)[Resumen](#eaaad)
  
### Introducción
  
El principal objetivo de este capítulo es proporcionar al lector una guía sobre cómo probar su propia implementación de la solución *Seguridad en LAN inalámbricas con PEAP y contraseñas*. Las recomendaciones que se ofrecen en este capítulo se basan en la experiencia obtenida por Microsoft® durante la prueba de esta solución.
  
En la primera parte del capítulo se describe el proceso de prueba que ha utilizado Microsoft. En la segunda parte se describen los escenarios de prueba que puede utilizar para comprobar una solución antes de implementarla en el entorno de producción. Los escenarios de prueba incluidos en este capítulo complementan los procedimientos de prueba de comprobación que se incluyen en los capítulos del 3 al 6.
  
#### Conocimientos previos necesarios
  
Para probar esta solución se recomienda tener conocimientos operativos en los siguientes campos:
  
-   Conceptos de la infraestructura de claves públicas y los Servicios de Certificate Server de Microsoft.
  
-   Servidores IAS (Servicio de autenticación de Internet) (servidor RADIUS).
  
-   Instalación de controladores de adaptadores de red inalámbrica y configuración de red inalámbrica en Microsoft Windows® XP.
  
-   Uso y configuración de Pocket PC 2003.
  
-   Servicio de directorio Microsoft Active Directory® (incluidas las herramientas de administración y estructura de Active Directory; el trabajo con usuarios, grupos y otros objetos de Active Directory, y las directivas de grupo).
  
-   Lenguaje Microsoft Windows® Scripting Host y Microsoft Visual Basic® Scripting Edition (VBScript) (serán muy útiles para personalizar o utilizar las secuencias de comandos y las herramientas que se incluyen con esta guía).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Cómo se ha probado la solución en Microsoft
  
El equipo de prueba de Microsoft se ha centrado en comprobar el perfil de la solución descrito en el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas". A continuación se describen las principales características del perfil:
  
-   Un bosque de Active Directory de un solo dominio que contenía dos controladores de dominio con el nivel funcional de dominio del modo nativo de Windows 2000.
  
-   Se instalaron servidores del controlador de dominio en Windows Server™ 2003, Standard Edition.
  
-   Se utilizaron Windows XP Service Pack 1 (Professional Edition y Tablet Edition) y Pocket PC 2003 (Hewlett Packard IPAQ 5550) como clientes inalámbricos.
  
-   Se instaló IAS en los controladores de dominio.
  
-   Se instaló el servidor de la entidad emisora de certificados en uno de los controladores de dominio.
  
-   La red del sitio de la oficina central se encontraba en una red de área local (LAN); el sitio de la sucursal se encontraba en otra LAN independiente.
  
-   Se utilizó la privacidad equivalente por cable (WEP) dinámica para la protección de datos de WLAN, en lugar de WPA.
  
-   La sucursal remota tenía una infraestructura formada sólo por puntos de acceso inalámbrico y se agregó latencia en la conexión con la oficina central para simular un tipo de conexión de módem por cable o DSL.
  
Este perfil no cubre todas las configuraciones posibles de la solución (por ejemplo, el escalado a un tamaño de organización mayor), pero se garantiza la prueba de todos los componentes de las configuraciones. Los cambios de arquitectura necesarios para escalar este perfil a una organización con 5000 usuarios son relativamente pequeños.
  
**Nota:** las pruebas que aquí se describen sólo incluyen la comprobación de la solución realizada por Microsoft. No se incluyen las pruebas ampliadas del producto realizadas por los grupos de productos de Microsoft; la prueba de la solución es una prueba adicional.
  
#### Prueba del diseño de red
  
El entorno del laboratorio de prueba se basó en el diseño de red descrito en el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas". En la siguiente figura se muestra el diseño físico del caso de prueba, que posee la configuración de red más sencilla descrita en el capítulo 2.
  
[![](images/Dd162271.PEAP_701(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_701_big(es-es,technet.10).gif)
  
**Figura 7.1. Arquitectura de red del laboratorio de pruebas**
  
La red de la oficina central era una única red con los clientes inalámbricos y los servidores de dominio en una subred. El sitio de la sucursal tenía una red independiente y estaba en otra subred. El enrutador que vinculaba la oficina central y la sucursal incluía latencia de WAN simulada y limitaciones de ancho de banda. Los puntos de acceso inalámbrico estaban suficientemente separados para que los usuarios pudieran desplazarse entre ellos.
  
Aunque se utilizó una única LAN sin segmentar para la prueba, se puede segregar la red interna utilizando distintas subredes, LAN virtuales (VLAN) y conmutadores para administrar mejor el rendimiento y la seguridad de la red.
  
Una vez desarrollada la red básica formada por controladores de dominio, el Sistema de nombres de dominio (DNS), el Protocolo de configuración dinámica de host (DHCP), los archivos, la impresión y los servicios Web con WEP inalámbrica estática, se utilizó la guía de implementación que se proporciona en los capítulos del 3 al 6 para instalar y configurar cada uno de los componentes. En estos capítulos se incluyen procedimientos de comprobación, que se ejecutan tal y como se describe. Se realizó un conjunto mayor de pruebas antes, durante y después de la creación. Los escenarios de prueba más importantes que se han utilizado se incluyen en la siguiente sección; puede utilizarlos para probar su implementación de la solución.
  
La solución creada, las secuencias de comandos de creación y de funcionamiento, y la documentación se sometieron a tres rondas de prueba y los problemas se trataron como errores. La prueba se consideró finalizada y satisfactoria cuando se resolvieron todos los errores.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Comprobación de la implementación
  
En esta sección se describen los principales escenarios de prueba utilizados por Microsoft para probar la solución.
  
Estos escenarios de prueba no son exhaustivos; puede desarrollar sus propios ejemplos adaptados a los requisitos de la organización. En este capítulo se han repetido algunos escenarios de comprobación descritos en capítulos anteriores para que la comprobación sea completa. Debe leer los capítulos anteriores antes de utilizar estos escenarios de prueba. Si la prueba falla en alguno de estos escenarios, consulte la sección "Solución de problemas" en el capítulo 8, "Mantenimiento de soluciones de seguridad en LAN inalámbricas" para diagnosticar y resolver los errores de la prueba.
  
#### Escenario 1: comprobación de la implementación de certificados de servidor IAS
  
En este escenario se comprueba que una vez creados y configurados los servidores IAS, éstos reciben el certificado de autenticación de servidor con inscripción automática de la entidad emisora de red.
  
**Detalles de ejecución**
  
1.  Abra un shell de comandos con el acceso directo MSS WLAN Tools.
  
2.  Ejecute el siguiente comando para abrir la MMC de **Certificados**:
  
    **ComputerCerts.msc**
  
3.  En el árbol de la consola, haga doble clic en **Certificados (equipo local)** y, a continuación, haga doble clic en **Personal**. A continuación, haga clic en **Certificados**.
  
4.  Debe aparecer al menos un certificado con el nombre del servidor IAS en la columna **Emitido para** y el nombre de la entidad emisora en la columna **Emitido por**. Desplácese por la lista (a la derecha) y compruebe que el valor de la **Plantilla de certificado** sea **Equipo** para este certificado.
  
5.  Si el certificado necesario no aparece en la MMC de **Certificados**, seleccione **Certificados (equipo local)** en el árbol de la consola del panel de la izquierda, haga clic en **Todas las tareas** en el menú **Acción** y, a continuación, haga clic en **Inscribir certificados automáticamente**. A continuación, actualice la vista de la MMC de **Certificados**.
  
#### Escenario 2: comprobación del certificado de entidad emisora raíz en el cliente inalámbrico Windows XP
  
En este escenario se comprueba que un cliente inalámbrico Windows XP válido recibe el certificado raíz de la entidad emisora de red en el almacén de entidades emisoras raíz de confianza. Este certificado se descarga y se agrega al almacén cuando se actualiza la directiva de grupo.
  
**Detalles de ejecución**
  
1.  Inicie la sesión en el equipo cliente como Administrador.
  
2.  Seleccione **Inicio, Ejecutar**, escriba **MMC.exe** y presione **Intro**.
  
3.  Desde el menú **Archivo** de MMC, seleccione **Agregar o quitar complemento**.
  
4.  En la ventana **Agregar o quitar complemento**, haga clic en el botón **Agregar**. Seleccione el elemento **Certificados** en la lista de complementos disponibles.
  
5.  Seleccione **Cuenta de equipo** y, a continuación, haga clic en **Siguiente**.
  
6.  Haga clic en **Finalizar**.
  
7.  Cierre las ventanas **Agregar un complemento independiente** y **Agregar o quitar complemento**.
  
8.  En el panel izquierdo, desplácese hasta Certificados (equipo local)\\Entidades emisoras raíz confiables\\Certificados.
  
9.  Busque el certificado de la entidad emisora, que aparecerá con el nombre que se le proporcionó durante la instalación de la entidad emisora.
  
10. Si el certificado no aparece en la lista, ejecute el siguiente comando en un símbolo del sistema:
  
    **Gpupdate /force**
  
11. Vuelva a la MMC de **Certificados**. Haga clic con el botón secundario en el nodo **Certificados (equipo local)**, seleccione **Actualizar** y vuelva a comprobar si aparece el certificado de la entidad emisora.
  
#### Escenario 3: comprobación de la autenticación de usuarios en la red inalámbrica
  
Éste es el escenario de prueba más importante. En él se comprueba que un usuario de la WLAN puede autenticarse y conectarse a la red después de instalar y configurar la solución.
  
**Detalles de ejecución**
  
1.  Asegúrese de que un usuario del dominio sea miembro del grupo Usuarios de LAN inalámbrica o del grupo Usuarios del dominio (que es miembro del primer grupo).
  
2.  El usuario deberá iniciar sesión en un equipo cliente que tenga una tarjeta de WLAN instalada y que no esté conectado a la red con cable. El usuario deberá proporcionar las credenciales del dominio durante el inicio de sesión.
  
3.  Abra el panel **Conexiones de red** desde el **Panel de control** y compruebe el estado de las **Conexiones de red inalámbricas**. Debería mostrar el estado **Autenticación satisfactoria** para la conexión inalámbrica.
  
4.  Desde el símbolo del sistema, utilice el comando ping para comprobar la conexión a través de la red con otro equipo de la misma.
  
5.  En el servidor IAS, abra **Visor de sucesos**. El registro de sucesos del **Sistema** debe contener un registro IAS de tipo de información del Id. de suceso 1. Examine la descripción del registro, que debe incluir los detalles de autenticación del usuario.
  
#### Escenario 4: comprobación de la autenticación de equipos en la red inalámbrica
  
En este escenario se comprueba que se ha autenticado un equipo en la red cuando el usuario no ha iniciado una sesión.
  
**Detalles de ejecución**
  
1.  Asegúrese de que la cuenta del equipo sea miembro del grupo Equipos de LAN inalámbrica o el grupo Equipos del dominio (que es miembro del primer grupo).
  
2.  Reinicie el equipo después de comprobar que tiene una tarjeta WLAN instalada y que no está conectado a la red con cable.
  
3.  Cuando aparezca el mensaje de inicio de sesión, no inicie la sesión y deje el equipo inactivo unos minutos.
  
4.  En el servidor IAS, abra **Visor de sucesos**. El registro de sucesos del **Sistema** debe contener un registro IAS de tipo de información del Id. de suceso 1 para el nombre de host del equipo. Examine la descripción del registro, que debe incluir los detalles de autenticación del equipo.
  
#### Escenario 5: comprobación de la autenticación de Pocket PC en la red inalámbrica
  
En este escenario se comprueba que un usuario puede iniciar una sesión en la red WLAN desde un dispositivo Pocket PC.
  
**Detalles de ejecución**
  
1.  Asegúrese de que un usuario del dominio sea miembro del grupo Usuarios de LAN inalámbrica o del grupo Usuarios del dominio (que es miembro del primer grupo).
  
2.  Habilite la conexión inalámbrica en Pocket PC y establezca la configuración de 802.1X en Pocket PC siguiendo las instrucciones que se incluyen en el capítulo 6, "Configuración de clientes de LAN inalámbricas".
  
3.  Mantenga seleccionado el nombre de la red en la lista de redes inalámbricas hasta que aparezca una opción de conexión. Elija **Conectar** para realizar la conexión.
  
4.  Cuando tenga que especificar las credenciales de domino en la pantalla **Inicio de sesión de red**, escriba el nombre, la contraseña y el dominio del usuario.
  
5.  Si la autenticación es satisfactoria, el icono de estado de la red no tendrá una cruz. Para comprobar el estado, abra **Internet Explorer** en el menú **Inicio** y examine un sitio Web cualquiera de la intranet.
  
6.  En el servidor IAS, abra **Visor de sucesos**. El registro de sucesos del **Sistema** debe contener un registro IAS de tipo de información del Id. de suceso 1. Consulte la descripción del registro, que debe incluir los detalles de autenticación del usuario.
  
#### Escenario 6: bloqueo de un cliente WLAN mediante la directiva de acceso remoto IAS
  
Este escenario se basa en las instrucciones proporcionadas en el capítulo 8, "Mantenimiento de soluciones de seguridad en LAN inalámbricas". Un administrador, si es necesario, puede bloquear el acceso inalámbrico de un usuario a la red utilizando la directiva de denegación de acceso remoto (este procedimiento se describe en la sección "Denegación del acceso a WLAN a un usuario o equipo" del capítulo 8). Configure la directiva de denegación de acceso remoto en los servidores IAS antes de ejecutar este escenario de prueba.
  
**Detalles de ejecución**
  
1.  Compruebe que la cuenta de un equipo particular sea miembro del grupo Denegar usuarios de LAN inalámbrica.
  
2.  El usuario deberá iniciar sesión en un equipo cliente que tenga una tarjeta de WLAN instalada y que no esté conectado a la red con cable. El usuario deberá introducir las credenciales del dominio al iniciar sesión.
  
3.  El usuario no podrá iniciar una sesión en el dominio; debe aparecer un mensaje de "acceso denegado".
  
4.  En el servidor IAS, abra **Visor de sucesos**. El registro de sucesos del **Sistema** debe contener un registro IAS de tipo de advertencia del Id. de suceso 2. Examine la descripción del registro, que debe incluir los detalles del error de autenticación del usuario.
  
#### Escenario 7: acceso a WLAN denegado si el usuario no es miembro de los grupos de acceso a la WLAN
  
En este caso se comprueba que se deniega el acceso inalámbrico a la red a un usuario si no es miembro del grupo Usuarios de LAN inalámbrica. Este método es una alternativa al bloqueo del acceso inalámbrico del usuario a la red.
  
**Detalles de ejecución**
  
1.  Abra la consola **Usuarios y equipos de Active Directory** en el panel **Herramientas administrativas**.
  
2.  Elimine el grupo Usuarios del dominio del grupo Usuarios de LAN inalámbrica, o elimine un usuario concreto si agrega los usuarios directamente al grupo Usuarios de LAN inalámbrica.
  
3.  El usuario deberá iniciar sesión en un equipo cliente que tenga una tarjeta de WLAN instalada y que no esté conectado a la red con cable. El usuario deberá introducir las credenciales del dominio al iniciar sesión.
  
4.  El usuario no podrá iniciar una sesión en la red; debe aparecer un mensaje de "acceso denegado".
  
5.  En el servidor IAS, abra **Visor de sucesos**. El registro de sucesos del **Sistema** debe contener un registro IAS de tipo de advertencia del Id. de suceso 2. Examine la descripción del registro, que debe incluir los detalles del error de autenticación del usuario.
  
#### Escenario 8: comprobación de la conmutación por error del servicio IAS
  
En este escenario de prueba se comprueba la disponibilidad del servicio IAS en los clientes inalámbricos cuando uno de los servidores IAS no está disponible. Este tipo de errores no debería provocar la interrupción de la conexión con la red de los clientes inalámbricos. Éste es un escenario de prueba importante en el que se comprueba que los puntos de acceso cambian a los servidores IAS secundarios cuando el servidor IAS principal no está disponible.
  
**Detalles de ejecución**
  
1.  Abra la MMC de **IAS** en el servidor IAS principal de la red y haga clic en el nombre del servidor. A continuación, detenga el servicio IAS haciendo clic en el botón **Detener** de la barra de menús.
  
2.  Utilice una cuenta de usuario de dominio con acceso autorizado a la WLAN e inicie una sesión en la red mediante una conexión inalámbrica.
  
3.  El usuario deberá poder autenticarse en la red y conectarse correctamente a ella. Para comprobarlo, abra el panel **Conexiones de red** desde el **Panel de control** y compruebe el estado de las **Conexiones de red inalámbricas**. El estado debería mostrar **Autenticación satisfactoria** para la conexión inalámbrica.
  
4.  Desde el símbolo del sistema, utilice el comando **ping** para comprobar la conexión a través de la red con otro equipo de la misma.
  
5.  En el servidor IAS secundario, abra **Visor de sucesos**. El registro de sucesos del **Sistema** debe contener un registro IAS de tipo de información del Id. de suceso 1. Examine la descripción del registro, que debe incluir los detalles de autenticación del usuario.
  
#### Escenario 9: desplazamiento de clientes inalámbricos entre puntos de acceso y reautenticación en la WLAN
  
En este escenario se comprueba que los clientes inalámbricos pueden desplazarse entre puntos de acceso, lo que provoca la reautenticación (o la reconexión rápida, si está habilitada). Es importante comprobar este escenario antes de implementar la solución en el entorno de producción. En esta prueba se comprueba que la conexión de la red inalámbrica no se interrumpe para los usuarios.
  
**Detalles de ejecución**
  
1.  Utilizando una cuenta de usuario de dominio con acceso autorizado a la WLAN, inicie una sesión en la red mediante una conexión inalámbrica. Compruebe que la conexión de red se ha realizado correctamente.
  
2.  En el servidor IAS, abra **Visor de sucesos**. El registro de sucesos del **Sistema** debe contener un registro IAS de tipo de información del Id. de suceso 1. Examine la descripción del registro, que debe incluir los detalles de autenticación del usuario.
  
3.  En los detalles de autenticación del usuario, busque la dirección IP del punto de acceso con el que esté conectado el usuario. Este valor aparece en el campo **Dirección IP del cliente**.
  
4.  Desplácese con el equipo a otra ubicación para que el cliente esté cerca de un punto de acceso vecino y lejos del punto de acceso con el que estaba conectado.
  
5.  Esto hará que el cliente Windows XP vuelva a autenticarse y se conecte con el nuevo punto de acceso.
  
6.  En el servidor IAS, abra **Visor de sucesos**. El registro de sucesos del **Sistema** debe contener un registro IAS de tipo de información del Id. de suceso 1. Examine la descripción del registro, que debe incluir los detalles de reautenticación del usuario; el campo **Dirección IP del cliente** debe incluir la dirección IP del nuevo punto de acceso.
  
#### Escenario 10: reautenticación del cliente inalámbrico porque se ha agotado el tiempo de espera de la sesión IAS
  
En este escenario se comprueba la rotación de claves WEP dinámicas configuradas en la directiva de solicitud de conexión IAS. En esta prueba se comprueba que los clientes se reautentican periódicamente (después del tiempo configurado) para que las claves WEP continúen cambiando.
  
**Detalles de ejecución**
  
1.  Utilizando una cuenta de usuario de dominio con acceso autorizado a la WLAN, inicie una sesión en la red mediante una conexión inalámbrica. Compruebe que la conexión de red se ha realizado correctamente.
  
2.  En el servidor IAS, abra **Visor de sucesos**. El registro de sucesos del **Sistema** debe contener un registro IAS de tipo de información del Id. de suceso 1. Examine la descripción del registro, que debe incluir los detalles de autenticación del usuario.
  
3.  Deje el cliente conectado a la red un período de tiempo superior a una hora. Puede iniciar una solicitud ICMP continua en otro equipo de la red para comprobar que la conexión está activada.
  
4.  Cuando transcurra la hora, abra **Visor de sucesos** y consulte el registro de sucesos del **Sistema**. El registro debe contener un registro IAS de tipo de información del Id. de suceso 1. Examine la descripción del registro, que debe incluir los detalles de reautenticación del usuario.
  
#### Escenario 11: alerta de correo electrónico de un error de copia de seguridad de IAS
  
En este caso de prueba se comprueba que las alertas de correo electrónico están correctamente configuradas para los servidores IAS, tal y como se describe en esta solución. Si se han implementado correctamente, estas alertas aumentan significativamente la capacidad de administración del servicio IAS, que es fundamental para la conectividad de la red inalámbrica. La situación ideal sería que esta prueba se realizase después de la implementación para confirmar que los servicios de notificación se ejecutan correctamente.
  
Para realizar la prueba en este escenario, se simula un error de copia de seguridad de IAS con el fin de crear las alertas de correo electrónico necesarias. Los pasos para configurar la copia de seguridad de IAS que se deben realizar en este escenario se proporcionan en el capítulo 8, "Mantenimiento de soluciones de seguridad en LAN inalámbricas". Antes de ejecutar este escenario de prueba, debe leer el capítulo 8 y configurar las secuencias de comandos.
  
**Detalles de ejecución**
  
1.  Abra un shell de comandos con el acceso directo MSS WLAN Tools.
  
2.  Edite el archivo **Constants.vbs** y establezca el parámetro **ALERT\_EMAIL\_ENABLED** en **True**.
  
3.  Configure el parámetro **ALERT\_EMAIL\_RECIPIENTS** con las direcciones de correo electrónico de las personas a las que se deba alertar.
  
4.  Configure el parámetro **ALERT\_EMAIL\_SMTP** con el nombre DNS o la dirección IP del servidor SMTP.
  
5.  Ejecute el siguiente comando de copia de seguridad de IAS en una carpeta que no exista:
  
    **MSSTools BackupIAS /path:** *C:\\RutaIASIncorrecta.*
  
6.  En el servidor IAS, abra **Visor de sucesos**.El registro de sucesos de la **Aplicación** debe contener un registro de operaciones IAS de tipo de error del Id. de suceso 211.
  
7.  Las personas identificadas para las alertas recibirán una alerta de correo electrónico.
  
#### Escenario 12: alerta de correo electrónico de un error de servicio de entidad emisora
  
Este escenario de prueba es parecido al de la alerta de un error de copia de seguridad de IAS. En él se comprueba que las alertas de correo electrónico se envían al personal de administración si falla el servicio de entidad emisora.
  
Los pasos para configurar la copia de seguridad de entidad emisora que se necesita en este escenario se proporcionan en el capítulo 8, "Mantenimiento de soluciones de seguridad en LAN inalámbricas". Antes de ejecutar este escenario de prueba, debe leer el capítulo 8 y configurar las secuencias de comandos necesarias.
  
**Detalles de ejecución**
  
1.  Abra un shell de comandos con el acceso directo MSS WLAN Tools.
  
2.  Edite el archivo **Constants.vbs** y establezca el parámetro **ALERT\_EMAIL\_ENABLED** en **True**.
  
3.  Configure el parámetro **ALERT\_EMAIL\_RECIPIENTS** con las direcciones de correo electrónico de las personas a las que se deba alertar.
  
4.  Configure el parámetro **ALERT\_EMAIL\_SMTP** con el nombre DNS o la dirección IP del servidor SMTP.
  
5.  Abra la **Entidad emisora de certificados** en el panel **Herramientas administrativas**. Haga clic en el nombre de la entidad emisora y seleccione **Acción**, **Todas las tareas** y **Detener servicio**.
  
6.  Abra la MMC de **Servicios** en el panel **Herramientas administrativas**.
  
7.  Haga clic con el botón secundario en **Servicios de Certificate Server** y seleccione **Propiedades**. Cambie el tipo de **Inicio** a **Deshabilitar** y haga clic en **Aceptar** para cerrar.
  
8.  Ejecute el siguiente comando de entidad emisora:
  
    **MSSTools CheckCA**
  
9.  En el servidor de entidad emisora, abra **Visor de sucesos**.El registro de sucesos de la **Aplicación** debe contener un registro de operaciones de la entidad emisora de tipo de error del Id. de suceso 1.
  
10. Las personas identificadas para las alertas recibirán una alerta de correo electrónico cuando falle el servicio de entidad emisora.
  
11. Invierta el tipo de **Inicio** de **Servicios de Certificate Server** a **Automático** en la MMC de **Servicios**.
  
12. Inicie el servicio en la MMC de **Entidad emisora de certificados** haciendo clic en el botón **Inicio** de la barra de menús.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Herramientas de la prueba
  
Las siguientes herramientas se han utilizado durante la prueba de esta solución. Algunas de estas herramientas también se han utilizado durante las fases de creación y mantenimiento:
  
1.  **Certutil:** ésta es una herramienta multipropósito que se utiliza para configurar la entidad emisora; volcar y visualizar información sobre la configuración de entidad emisora; hacer copias de seguridad y restaurar componentes de entidad emisora; y comprobar certificados, pares de claves y cadenas de certificados.
  
2.  **Dcdiag:** esta herramienta analiza el estado de los controladores de dominio en un bosque o empresa.
  
3.  **Visor de registro de sucesos:** esta herramienta supervisa y captura los registros relacionados con las aplicaciones, la seguridad y el sistema.
  
4.  **Consola de administración de directivas de grupo:** esta herramienta se utiliza para visualizar y editar objetos de directiva de grupo en Active Directory.
  
5.  **NetMon:** esta utilidad captura y filtra las tramas del tráfico de red hacia y desde el equipo en el que está instalada. Esta herramienta no es necesaria directamente, pero es muy útil en la depuración de problemas de autenticación. Esta herramienta se puede instalar desde el **Panel de control** seleccionando **Agregar o quitar componente**, **Componentes de Windows**, **Herramientas de administración y supervisión** y **Herramientas del monitor de red**.
  
6.  **Netsh:** ésta es una utilidad de secuencia de comandos de línea de comandos que permite visualizar o modificar, ya sea de forma local o remota, la configuración de red de un equipo en ejecución. Es una herramienta multipropósito que se utiliza en las operaciones relacionadas con IAS.
  
7.  **Copia de seguridad de Windows:** ésta es la herramienta de copia de seguridad y restauración proporcionada con Windows que realiza operaciones de copia de seguridad y restauración en archivos, carpetas y el estado del sistema. Esta herramienta se puede ejecutar con un asistente o una línea de comandos.
  
8.  **PerfMon:** esta herramienta permite ver los registros de rendimiento del sistema y los contadores. Puede utilizar esta herramienta para supervisar el rendimiento de IAS.
  
9.  **Ping:** esta herramienta comprueba la conectividad de nivel IP con otro equipo TCP/IP mediante el envío de mensajes de solicitud de eco de ICMP. Los mensajes correspondientes de respuesta de eco que se reciben se visualizan con tiempos de retorno.
  
10. **Schtasks:** esta herramienta programa comandos y programas para que se ejecuten periódicamente o a una hora determinada. Agrega y elimina tareas de la programación, inicia y detiene tareas a petición, y visualiza y cambia tareas programadas.
  
La mayoría de estas herramientas se instalan automáticamente cuando se instala el sistema operativo Windows. La instalación del resto de herramientas se describe en el capítulo 3, "Preparación del entorno".
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Este capítulo trata sobre la prueba de seguridad de la solución WLAN. En la primera parte del capítulo se describen brevemente los parámetros utilizados por Microsoft para probar esta solución en la fase de desarrollo. En la segunda parte se incluyen las instrucciones para realizar algunos de los escenarios de prueba más importantes que se utilizan para probar esta solución. Estos escenarios de prueba permiten comprobar el funcionamiento correcto de la infraestructura de seguridad de WLAN antes de implementarla en un entorno de producción.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 8: Mantenimiento de soluciones de seguridad en LAN inalámbricas
  
[](#eiaae)[Introducción](#eiaae)  
[](#ehaae)[Información general](#ehaae)  
[](#egaae)[Requisitos previos del capítulo](#egaae)  
[](#efaae)[Tareas de mantenimiento esenciales](#efaae)  
[](#eeaae)[Funcionamiento de la infraestructura de WLAN](#eeaae)  
[](#edaae)[Solución de problemas](#edaae)  
[](#ecaae)[Resumen](#ecaae)  
[](#ebaae)[Referencias](#ebaae)
  
### Introducción
  
Este capítulo trata los procedimientos operativos relacionados con la administración de la solución *Seguridad en LAN inalámbricas con PEAP y contraseñas*. Este capítulo contiene instrucciones sobre las tareas operativas y de soporte técnico esenciales que necesita llevar a cabo para mantener la infraestructura de seguridad en la red de área local inalámbrica (WLAN), incluidos los servidores del Servicio de autenticación de Internet (IAS), las entidades emisoras de certificados, los puntos de acceso inalámbrico y los clientes WLAN. No obstante, este capítulo no incluye información sobre la administración general de la red o sobre la administración de otros aspectos que no sean servicios de seguridad, como el análisis y la optimización del tráfico en la red.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Información general
  
Las secciones más importantes de este capítulo son:
  
-   **Tareas de mantenimiento esenciales:** en esta sección se enumeran las tareas clave que necesita poner en práctica para instalar el sistema de administración (por ejemplo, configurar trabajos de copias de seguridad), y aquéllas que necesita llevar a cabo de forma regular para mantener el sistema (por ejemplo, tareas semanales de reorganización de archivos).
  
-   **Funcionamiento de la infraestructura de WLAN:** esta sección es, ante todo, una sección de referencia donde se detallan los diferentes tipos de tareas que ha de llevar a cabo para mantener la estructura de seguridad de WLAN. Los apartados contienen información sobre tareas operativas estándar, implementación de cambios, tareas de soporte técnico y de optimización.
  
-   **Solución de problemas:** esta sección contiene procedimientos y diagramas de flujo que sirven para solucionar problemas comunes que pueden surgir con la infraestructura de WLAN. Asimismo, incluye descripciones de herramientas y procedimientos útiles destinados a la solución de problemas que permiten habilitar el registro de distintos componentes.
  
-   **Referencias:** en esta sección se enumeran las fuentes de información adicional mencionadas en el texto.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Requisitos previos del capítulo
  
Debe estar familiarizado con la administración de Microsoft® Windows® Server™ 2003 o de Windows® 2000 Server. Las siguientes áreas son particularmente importantes:
  
-   Funcionamiento y mantenimiento básicos de Microsoft Windows Server 2003, incluido el uso de herramientas como Visor de sucesos, Administración de equipos y NTBackup.
  
-   IAS.
  
-   Servicios de Certificate Server.
  
-   Servicio de directorio Microsoft Active Directory® (incluidas las herramientas y la estructura de Active Directory), administración de usuarios, grupos y otros objetos de Active Directory, así como el uso de la directiva de grupo.
  
-   Conceptos de seguridad del sistema Windows como usuarios, grupos, auditorías, listas de control de acceso, uso de plantillas de seguridad y aplicación de éstas utilizando directivas de grupo o herramientas de línea de comandos.
  
-   LAN inalámbricas y conceptos de red generales.
  
-   Conocimientos de Windows Script Host y de Microsoft Visual Basic® Scripting Edition (VBScript) que ayudarán a comprender y a utilizar las secuencias de comandos que la solución proporciona.
  
Además, es recomendable que haya leído los siguientes capítulos para adquirir un buen conocimiento de la arquitectura y diseño de la solución:
  
-   Capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas"
  
-   Capítulo 3, "Preparación del entorno"
  
-   Capítulo 4, "Creación de la entidad emisora de certificados de red"
  
-   Capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas"
  
-   Capítulo 6, "Configuración de clientes de LAN inalámbricas"
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Tareas de mantenimiento esenciales
  
En esta sección se enumeran las tareas clave que debe realizar para que la infraestructura de WLAN funcione satisfactoriamente. Estas tareas se pueden dividir en dos categorías:
  
-   Tareas de configuración iniciales
  
-   Tareas de mantenimiento continuas
  
En esta sección también se enumeran las herramientas y las tecnologías utilizadas en los procedimientos de este capítulo.
  
#### Tareas de configuración iniciales
  
La siguiente tabla muestra las tareas que se deben realizar para poner en funcionamiento la infraestructura de seguridad de WLAN.
  
**Tabla 8.1. Tareas de configuración iniciales**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de la tarea</th>
<th style="border:1px solid black;" >Sección</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Configuración de la copia de seguridad de IAS</td>
<td style="border:1px solid black;">Tareas operativas</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Configuración de los tipos de alerta</td>
<td style="border:1px solid black;">Supervisión</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Habilitación de la supervisión de IAS</td>
<td style="border:1px solid black;">Supervisión</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Habilitación de la supervisión de la entidad emisora</td>
<td style="border:1px solid black;">Supervisión</td>
</tr>
</tbody>
</table>
  
#### Tareas de mantenimiento
  
La siguiente tabla muestra las tareas que se deben realizar con regularidad para mantener el funcionamiento de la infraestructura de seguridad de WLAN de forma adecuada. Puede utilizar esta tabla para planear los recursos necesarios y el programa operativo relacionados con la administración del sistema.
  
**Tabla 8.2. Tareas de mantenimiento**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de la tarea</th>
<th style="border:1px solid black;" >Frecuencia</th>
<th style="border:1px solid black;" >Sección</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Prueba de las copias de seguridad</td>
<td style="border:1px solid black;">6 meses</td>
<td style="border:1px solid black;">Tareas operativas</td>
</tr>
</tbody>
</table>
  
#### Herramientas y tecnología requeridas
  
En la tabla siguiente se enumeran las herramientas o tecnologías utilizadas en los procedimientos descritos en este capítulo.
  
**Tabla 8.3. Tecnología requerida**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre del elemento</th>
<th style="border:1px solid black;" >Fuente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Consola de administración (MMC) de usuarios y equipos de Active Directory</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MMC de la Entidad emisora de certificados</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Certutil.exe</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">DCDiag.exe</td>
<td style="border:1px solid black;">Herramientas de soporte técnico de Windows Server 2003</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">DSquery.exe</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Visor de sucesos</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Consola de administración de directivas de grupo</td>
<td style="border:1px solid black;">Descarga Web desde Microsoft.com</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MSS WLAN Tools</td>
<td style="border:1px solid black;">Secuencias de comandos instaladas como parte de esta solución</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Netdiag.exe</td>
<td style="border:1px solid black;">Herramientas de soporte técnico de Windows Server 2003</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Monitor de rendimiento</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Estado de la infraestructura de claves públicas</td>
<td style="border:1px solid black;">Kit de recursos de Windows Server 2003</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Medios extraíbles para la creación de copias de seguridad de entidad emisora raíz</td>
<td style="border:1px solid black;">CD-RW o cinta</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SchTasks.exe</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Editor de texto</td>
<td style="border:1px solid black;">Bloc de notas: Windows Server 2003</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Copia de seguridad de Windows</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servicio Programador de tareas de Windows</td>
<td style="border:1px solid black;">Windows Server 2003</td>
</tr>
</tbody>
</table>
  
**Tabla 8.4. Tecnología recomendada**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre del elemento</th>
<th style="border:1px solid black;" >Fuente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Infraestructura de correo electrónico (para alertas operativas)</td>
<td style="border:1px solid black;">Servidor y cliente SMTP/POP3/IMAP, por ejemplo Microsoft Exchange Server y Microsoft Outlook®</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Consola de alertas operativas</td>
<td style="border:1px solid black;">Microsoft Operations Manager u otro sistema de supervisión de servicios</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Distribución de actualizaciones de sistemas operativos</td>
<td style="border:1px solid black;">Microsoft Systems Management Server (SMS) o Microsoft Software Update Service (SUS)</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Funcionamiento de la infraestructura de WLAN
  
Esta sección incluye las tareas principales que necesita llevar a cabo para mantener la infraestructura de seguridad de WLAN.
  
#### Tareas operativas
  
Las tareas operativas abarcan los trabajos que hay que realizar regularmente para mantener el funcionamiento de la infraestructura de WLAN de forma adecuada.
  
##### Copias de seguridad de IAS y la entidad emisora de certificados
  
Debe realizar copias de seguridad de los servidores IAS regularmente, incluido el servidor IAS que ejecuta la entidad emisora de certificados. IAS requiere un procedimiento especial para exportar sus configuraciones a un archivo, del cual se puede realizar después una copia de seguridad normal. Puede realizar copias de seguridad de Servicios de Certificate Server utilizando la copia de seguridad del estado del sistema de Windows, disponible en la herramienta de copias de seguridad de Windows. Deberá establecer procedimientos de creación de copias de seguridad adecuados en todos los servidores en los que se esté ejecutando IAS.
  
Los dos procedimientos siguientes no se excluyen entre sí, sino que deberá configurar una copia de seguridad tanto de IAS como del servidor.
  
###### Configuración de la copia de seguridad de IAS
  
Ha de crear una carpeta con permisos restringidos a la que se exportará la configuración de IAS cada noche. También ha de crear un trabajo programado que ejecute cada noche la copia de seguridad de IAS (la secuencia de comandos de copia de seguridad no necesita que IAS se encuentre apagado para realizar la copia). Si la copia de seguridad se realiza correctamente, se escribirá un suceso en el registro de aplicaciones de Windows. En caso de error en la copia, se registrará un suceso de error.
  
**Precaución:** los archivos de seguridad de IAS incluyen todos los secretos de los clientes RADIUS. Se trata de una información extremadamente confidencial, por lo que debería tener cuidado y almacenar los datos en cuestión de forma segura.
  
**Para configurar la copia de seguridad de IAS**
  
1.  Abra un shell de comandos en el servidor utilizando el acceso directo de **MSS WLAN Tools** e introduzca el siguiente comando para crear una carpeta en la que guardar la configuración de IAS:
  
    **md** **c:\\IASBackup**
  
    La configuración de IAS suele ser menor de 100 KB y se puede guardar en la unidad del sistema, tal y como se muestra en el comando.
  
2.  Utilice el siguiente comando para establecer permisos para la carpeta de forma que sólo los administradores y operadores de copias de seguridad puedan leer y modificar el contenido:
  
    **cacls c:\\IASBackup /G system:F administrators:F "Backup Operators":C**
  
    Es probable que este comando se divida en varias líneas en este documento, pero debe escribirlo como una sola línea.
  
3.  Pruebe la copia de seguridad con la ayuda del siguiente comando:
  
    **"C:\\Archivos de programa\\Microsoft\\Microsoft WLAN-PEAP Tools\\msstools.cmd" BackupIAS /path:C:\\IASBackup**
  
    Es probable que este comando se divida en varias líneas en este documento, pero debe escribirlo como una sola línea. "**Microsoft WLAN-PEAP Tools**" contiene dos espacios incrustados: uno después de "Microsoft" y otro después de "WLAN-PEAP".
  
    **Nota:** si la copia de seguridad se realiza correctamente, se escribirá un suceso en el registro de aplicaciones de Windows y en la pantalla. En caso contrario, se registrarán sucesos de error.
  
4.  Cree una tarea programada que ejecute cada noche la exportación de la configuración de IAS. Por ejemplo, el siguiente comando programa un trabajo para ejecutarlo a las 22:00 horas cada noche:
  
    **SCHTASKS /Create /RU system /SC Daily /TN "IAS Backup"/TR "\\"C:\\Archivos de programa\\Microsoft\\Microsoft WLAN-PEAP Tools\\msstools.cmd\\" BackupIAS /path:C:\\IASBackup" /ST 22:00**
  
    Es probable que este comando se divida en varias líneas en este documento, pero debe escribirlo como una sola línea. "**Microsoft WLAN-PEAP Tools**" contiene dos espacios incrustados: uno después de "Microsoft" y otro después de "WLAN-PEAP".
  
    **Nota:** adjuntar la ruta al archivo de secuencias de comandos msstools.cmd entre barras diagonales inversas (\\) garantiza que el shell de comandos de Windows no va a interpretar las comillas dobles ("), ni las va a quitar del comando. El comando que admite y almacena el programador de tareas es el que se muestra en el paso 3.
  
###### Realización de copias de seguridad del servidor
  
Una vez establecida la tarea programada para realizar la copia de seguridad de IAS en el disco, debe configurar también una copia de seguridad regular, en un medio extraíble o en una ubicación de red, del estado del sistema del servidor y de los archivos de la configuración de IAS exportados. La forma más sencilla de llevarlo a cabo es utilizar la herramienta integrada de copias de seguridad de Windows. En caso de usar un sistema de copias de seguridad diferente, debe comprobar si incluye la funcionalidad equivalente a las copias de seguridad del estado del sistema de Windows. Esta información debe reflejarse en la documentación del sistema de copias de seguridad en cuestión. Una copia de seguridad del estado del sistema (o equivalente) es esencial para realizar correctamente copias de seguridad de las claves de Active Directory y del Servicio Certificate Server, así como de las bases de datos de certificados.
  
Si el software de copias de seguridad no incluye la funcionalidad de copias de seguridad del estado del sistema de Windows, puede efectuar los siguientes pasos:
  
-   Configure la herramienta de copias de seguridad de Windows para que realice una copia de seguridad del estado del sistema en un archivo del servidor (debe asegurarse de que tiene suficiente espacio libre, dado que esta copia ocupará 500 MB o más). Consulte la ayuda en línea de esta herramienta para obtener más detalles sobre este paso.
  
-   Configure el software de copias de seguridad para que copie el archivo de la copia de seguridad del estado del sistema, así como el archivo de la copia de seguridad de IAS descrito en el procedimiento anterior.
  
Para garantizar que las copias de seguridad son seguras y consistentes, efectúe lo siguiente:
  
-   Programe las distintas operaciones de copia de seguridad de forma que no se superpongan o, de lo contrario, se arriesgará a dañar los datos de las copias.
  
-   Comience las copias de seguridad del estado del sistema y del servidor con al menos 10 minutos de diferencia con respecto a las copias de IAS.
  
-   Si está realizando copias de seguridad del estado del sistema y del archivo del servidor de forma separada, deje que transcurra al menos una hora antes de comenzar con la copia del archivo del servidor para que finalice la copia del estado del sistema.
  
-   Almacene siempre una copia reciente de los datos de la copia de seguridad en una ubicación física distinta a la del servidor del que se ha realizado la copia. Así, podría recuperar el servidor si el equipo informático del sitio se destruyera o si no se pudiera tener acceso a él.
  
    **Precaución:** estos datos son confidenciales porque contienen secretos de RADIUS de todos los puntos de acceso en el servidor, de todo el material clave privado de la entidad emisora de certificados y de la base de datos de Active Directory. Debe transportar y almacenar los medios de copias de seguridad con la mayor protección posible, ya que el acceso no autorizado a esta información podría comprometer la seguridad de toda la organización.
  
##### Prueba de las copias de seguridad
  
Para comprobar las copias de seguridad del sistema de forma adecuada, sólo tiene que restaurarlas en un servidor de prueba y comprobar que el servidor restaurado funciona como se espera. La copia de seguridad del estado del sistema se debe restaurar en un sistema con un diseño de disco idéntico al del servidor del que se ha realizado la copia. Por ejemplo, Windows debe estar instalado en la misma ruta tanto en el servidor original como en el de prueba, al tiempo que el diseño de la unidad en la que se almacenan los archivos de Windows (como los archivos de paginación) debe ser igualmente idéntico en ambos.
  
**Importante:** para evitar conflictos con el nombre y las direcciones IP entre ambos servidores, el servidor de prueba se debe mantener sin conexión desde el momento en el que comienza la restauración del estado del sistema.
  
**Para restaurar el servidor**
  
1.  Prepare un servidor de restauración en el que quiera restaurar las copias de seguridad. En él, tendrá que utilizar la misma edición de Windows Server 2003 que en el servidor original. También debe instalar las secuencias de comandos de la solución en este servidor. Para obtener más información, consulte la sección "Instalación de herramientas de la solución" en el capítulo 3, "Preparación del entorno".
  
2.  Si usa copias de seguridad del estado del sistema y de los archivos por separado, utilice el software de copias de seguridad para restaurar los archivos de las copias de seguridad del estado del sistema y los de la configuración de IAS desde el medio de copia de seguridad al servidor. La configuración de IAS se debe restaurar en la misma ruta: C:\\IASBackup.
  
3.  Ejecute la utilidad de copias de seguridad de Windows y seleccione el archivo de la copia de seguridad del estado del sistema restaurado. Deberá pertenecer a un grupo que posea derechos de creación de copias de seguridad y restauración en el equipo (como Operadores de copia de seguridad o Administradores).
  
4.  Haga clic en **Restaurar**.
  
5.  Reinicie el sistema.
  
6.  Una vez reiniciado, compruebe que el funcionamiento es el esperado y que Active Directory y los Servicios de Certificate Server se han iniciado sin errores (probablemente se produzcan errores en el registro de sucesos, dado que el servidor no está conectado a la red).
  
7.  Utilice el acceso directo **MSS WLAN Tools** para abrir el shell de comandos. Para restaurar la configuración de IAS, ejecute el siguiente comando:
  
    **MSSTools RestoreIAS /path:C:\\IASBackup**
  
8.  Para comprobar que la configuración de IAS se ha restaurado, abra la consola de administración de IAS y compruebe los clientes RADIUS y las carpetas de directivas de acceso remoto.
  
#### Supervisión
  
Esta sección describe la supervisión de los componentes de IAS y de la entidad emisora de certificados de la infraestructura de seguridad de WLAN. No incluye información sobre la supervisión de los puntos de acceso inalámbrico o de otros dispositivos de red, ni ofrece consejos generales sobre la supervisión de servidores de Windows. Para obtener más información sobre la supervisión de servidores de Windows, consulte la sección "Referencias" al final del capítulo.
  
En gran parte de los procedimientos de esta sección se emplean secuencias de comandos de supervisión automatizadas que se obtienen junto con la solución. Si estas secuencias de comandos detectan un error, desencadenarán una alerta y, en algunos casos, intentarán recuperarse del mismo.
  
##### Configuración de los tipos de alerta
  
Cualquier alerta de las secuencias de comandos de supervisión se puede enviar al registro de aplicaciones de Windows, a uno o más destinatarios de correo electrónico o a ambos. Antes de habilitar las herramientas de supervisión, ha de especificar los tipos de alerta que desea. Además, si ha optado por enviar alertas por correo electrónico, debe proporcionar las direcciones de correo electrónico de los destinatarios y el nombre del servidor de correo al que desea enviar los mensajes.
  
Para especificar estos parámetros, es preciso modificar el archivo constants.vbs. A continuación se muestran las secciones más importantes de este archivo con los elementos que probablemente desee cambiar en *cursiva*:
  
```  
Parámetros de alerta CONST ALERT\_EMAIL\_ENABLED = FALSE 'establecido en habilitar/deshabilitar correo electrónico CONST ALERT\_EVTLOG\_ENABLED = TRUE 'establecido en habilitar/deshabilitar entradas del registro de sucesos ' establecido en lista de destinatarios de alertas de correo electrónico separados por comas CONST ALERT\_EMAIL\_RECIPIENTS = "Admin@woodgrovebank.com,Ops@woodgrovebank.com" 'servidor SMTP que se va a utilizar (use el nombre DNS o la dirección IP) CONST ALERT\_EMAIL\_SMTP = "mail.woodgrovebank.com"   
```  
##### Supervisión de IAS
  
IAS registrará varios sucesos en el registro del sistema de Windows. Éstos incluyen notificaciones de inicio y de término del servicio (y todos los errores o advertencias asociados), así como notificaciones de intentos de autenticación. Las entradas del registro de solicitud de autenticación se describen en detalle en la sección "Solución de problemas" de este capítulo.
  
###### Habilitación de la supervisión de IAS
  
Esta solución incluye una sencilla secuencia de comandos que supervisa el nivel de respuesta de IAS. La secuencia de comandos comprueba si el proceso de IAS se está ejecutando. Si es así, la secuencia de comandos intenta consultar a IAS empleando la interfaz **Objetos de datos del servidor**. Si alguna de estas comprobaciones presenta errores, la secuencia de comandos emitirá una alerta.
  
**Nota:** la secuencia de comandos de supervisión no comprueba que la autenticación RADIUS sea correcta; sólo comprueba el nivel de respuesta general del proceso de IAS. Para comprobar las operaciones de RADIUS de forma integral, necesita un cliente RADIUS para emular los puntos de acceso inalámbrico que transfieren la solicitud del cliente WLAN.
  
El procedimiento siguiente describe cómo configurar la secuencia de comandos de supervisión para que se ejecute como tarea programada, a fin de que las alertas se emitan de forma automática si IAS deja de responder. No obstante, dado que la secuencia se ejecuta en el mismo servidor, es obvio que no podrá avisarle si se produce un error de carácter general en el servidor. En consecuencia, deberá supervisar también los servidores para asegurarse de que funcionan y responden. Para configurar la ejecución de la secuencia de comandos como una tarea programada en cada servidor IAS, deberá realizar el siguiente procedimiento:
  
Cada vez que se detecte un error, se enviará una alerta por correo electrónico (si se han configurado las alertas por correo electrónico) y se registrará un suceso en el registro de aplicaciones (consulte la tabla de la sección siguiente para obtener más detalles sobre los tipos de sucesos registrados). A diferencia de la secuencia de comandos de supervisión de la entidad emisora de certificados, no se intentará reiniciar IAS para corregir los problemas. Esto se debe a que IAS debe autenticar clientes WLAN continuamente (cosa que no sucede con la entidad emisora). Permitir que la secuencia de comandos de supervisión reinicie IAS a ciegas puede ocasionar problemas en lugar de resolverlos. En su lugar, permanezca atento a cualquier alerta generada por la secuencia y realice el diagnóstico adecuado de la causa de la alerta antes de intentar resolver el problema manualmente.
  
**Para configurar la supervisión de IAS**
  
1.  Abra un shell de comandos utilizando el acceso directo **MSS WLAN Tools**.
  
2.  Ejecute el siguiente comando para programar la ejecución de la secuencia de comandos cada noche a las 1:30 horas (se ejecuta 30 minutos después de la hora para compensar el trabajo de copia de seguridad de IAS).
  
    **SCHTASKS /Create /RU system /SC Hourly /TN "IAS Check"/TR "\\"C:\\Archivos de programa\\Microsoft\\Microsoft WLAN-PEAP Tools\\msstools.cmd\\" CheckIAS" /ST 1.30**
  
    Es probable que este comando se divida en varias líneas en este documento, pero debe escribirlo como una sola línea. "**Microsoft WLAN-PEAP Tools**" contiene dos espacios incrustados: uno después de "Microsoft" y otro después de "WLAN-PEAP".
  
    **Nota:** adjuntar la ruta al archivo de secuencias de comandos msstools.cmd entre barras diagonales inversas (\\) garantiza que el shell de comandos de Windows no va a interpretar las comillas dobles ("), ni las va a quitar del comando. El uso de barras diagonales inversas (\\) antes de las comillas (") garantiza que el comando que el programador de tareas admite y almacena es el mostrado en el paso 2.
  
###### Sucesos IAS registrados por las secuencias de comandos de MSS
  
La secuencia de comandos de supervisión y la de copia de seguridad de IAS registran los siguientes tipos de sucesos en el registro de sucesos.
  
**Tabla 8.5. Sucesos IAS devueltos por las secuencias de comandos de herramientas de IAS en esta solución**

 
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Suceso IAS</th>
<th style="border:1px solid black;" >Importancia</th>
<th style="border:1px solid black;" >Categoría del suceso</th>
<th style="border:1px solid black;" >Origen del suceso</th>
<th style="border:1px solid black;" >Id. de suceso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Copia de seguridad de IAS realizada</td>
<td style="border:1px solid black;">Copia de seguridad de la configuración de IAS en el archivo realizada correctamente.</td>
<td style="border:1px solid black;">Información</td>
<td style="border:1px solid black;">Operaciones de IAS</td>
<td style="border:1px solid black;">210</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Ruta de la copia de seguridad de IAS no válida</td>
<td style="border:1px solid black;">Error en la copia de seguridad por haber especificado una ruta de destino no válida</td>
<td style="border:1px solid black;">Error</td>
<td style="border:1px solid black;">Operaciones de IAS</td>
<td style="border:1px solid black;">211</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">IAS no tiene acceso a la ruta de copia de seguridad</td>
<td style="border:1px solid black;">Error en la copia de seguridad porque los archivos no se pudieron escribir en la ruta de destino especificada.</td>
<td style="border:1px solid black;">Error</td>
<td style="border:1px solid black;">Operaciones de IAS</td>
<td style="border:1px solid black;">212</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Restauración de IAS realizada</td>
<td style="border:1px solid black;">Configuración de IAS correctamente restaurada a partir de la configuración guardada</td>
<td style="border:1px solid black;">Información</td>
<td style="border:1px solid black;">Operaciones de IAS</td>
<td style="border:1px solid black;">220</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Error en la restauración de IAS</td>
<td style="border:1px solid black;">Error en la restauración de la configuración de IAS</td>
<td style="border:1px solid black;">Advertencia</td>
<td style="border:1px solid black;">Operaciones de IAS</td>
<td style="border:1px solid black;">221</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Error en la consulta de directiva de IAS</td>
<td style="border:1px solid black;">No se pudo establecer contacto con IAS mediante la interfaz de objetos de datos de servidor. Puede que IAS no se esté ejecutando.</td>
<td style="border:1px solid black;">Error</td>
<td style="border:1px solid black;">Operaciones de IAS</td>
<td style="border:1px solid black;">230</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Directivas de IAS no detectadas</td>
<td style="border:1px solid black;">IAS no contiene ninguna directiva de acceso remoto.
Esto no debería suceder en un servidor IAS configurado de la forma habitual y, probablemente, indique la existencia de otro problema relacionado con IAS o con la red.</td>
<td style="border:1px solid black;">Error</td>
<td style="border:1px solid black;">Operaciones de IAS</td>
<td style="border:1px solid black;">231</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">IAS no instalado</td>
<td style="border:1px solid black;">IAS no está instalado en el equipo.</td>
<td style="border:1px solid black;">Error</td>
<td style="border:1px solid black;">Operaciones de IAS</td>
<td style="border:1px solid black;">232</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">IAS se ha detenido</td>
<td style="border:1px solid black;">El servicio IAS no se estaba ejecutando, pero se inició correctamente.</td>
<td style="border:1px solid black;">Advertencia</td>
<td style="border:1px solid black;">Operaciones de IAS</td>
<td style="border:1px solid black;">233</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">IAS no se está ejecutando</td>
<td style="border:1px solid black;">Error al intentar iniciar el servicio IAS</td>
<td style="border:1px solid black;">Error</td>
<td style="border:1px solid black;">Operaciones de IAS</td>
<td style="border:1px solid black;">234</td>
</tr>
</tbody>
</table>
  
##### Supervisión de la entidad emisora de certificados
  
La entidad emisora de certificados exige relativamente poca atención más allá de la supervisión del estado general del servidor y de la correcta realización de las copias de seguridad. En esta solución, la entidad emisora de certificados sólo es necesaria para tareas relativamente poco comunes como la emisión de certificados para servidores IAS nuevos y la renovación anual de certificados existentes. En definitiva, la entidad emisora de certificados no es un servicio fundamental.
  
La entidad emisora de certificados publica también una lista de los certificados que el administrador revoca. Esta lista, conocida como lista de revocación de certificados, se publica semanalmente en Active Directory. Dado que la entidad emisora de certificados emite un número pequeño de certificados, la lista de revocación de certificados también será pequeña y, por lo general, estará vacía. A pesar de esto, es importante que se publique en Active Directory de manera regular para que, así, las aplicaciones puedan comprobar el estado de revocación de todo certificado emitido por la entidad emisora. Por ejemplo, la propia entidad emisora de certificados tiene que comprobar el estado de revocación de cualquier certificado que emita antes de enviarlo a quien lo haya solicitado.
  
La secuencia de comandos de supervisión de la entidad comprueba que ésta está respondiendo a las solicitudes y que hay una lista de revocación de certificados disponible en Active Directory. Si se produce error en cualquiera de estas comprobaciones, la secuencia de comandos intentará reiniciar la entidad emisora de certificados. En caso de que el error se produzca en la lista, intentará igualmente publicar una nueva. Si el error se detecta incluso después de estos intentos de recuperación, se generará una alerta que se enviará por correo electrónico a la cuenta configurada y se escribirá en el registro de sucesos.
  
###### Habilitación de la supervisión de la entidad emisora de certificados
  
El siguiente procedimiento describe cómo configurar la secuencia de comandos de supervisión para que se ejecute como tarea programada de forma que, en caso de error, las alertas se emitan de forma automática y se intente la recuperación. Esta secuencia de comandos ha de ejecutarse sólo en el servidor de la entidad emisora de certificados.
  
**Para configurar la secuencia de comandos de supervisión de la entidad emisora de certificados**
  
1.  Abra un shell de comandos utilizando el acceso directo **MSS WLAN Tools**.
  
2.  Ejecute el siguiente comando para programar la ejecución de la secuencia de comandos cada noche a las 1:20 horas (se programa la ejecución a los 20 minutos después de la hora para compensar otras tareas programadas).
  
    **SCHTASKS /Create /RU system /SC Hourly /TN "CA Check" /TR "\\"C:\\Archivos de programa\\Microsoft\\Microsoft WLAN-PEAP Tools\\msstools.cmd\\" CheckCA" /ST 01:20**
  
    Es probable que este comando se divida en varias líneas en este documento, pero debe escribirlo como una sola línea.
  
    **Nota:** adjuntar la ruta completa del archivo de secuencias de comandos msstools.cmd entre barras diagonales inversas (\\) asegura que el shell de comandos de Windows no va a interpretar las comillas dobles ("), ni las va a quitar del comando. La ruta que el programador de tareas almacena debe adjuntarse entre comillas si incluye espacios incrustados (como en "Archivos de programa"). El uso de una barra diagonal inversa (\\) antes de las comillas (") garantiza que la ruta que el programador de tareas almacena se adjunte entre comillas dobles.
  
###### Sucesos de la entidad emisora registrados por las secuencias de comandos de MSS
  
La secuencia de comandos de supervisión de la entidad emisora de certificados registra lo siguiente en el registro de sucesos:
  
**Tabla 8.6. Sucesos de la entidad emisora que las secuencias de comandos de supervisión de la entidad emisora de certificados devuelve en esta solución**

 
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Suceso de la entidad emisora</th>
<th style="border:1px solid black;" >Importancia</th>
<th style="border:1px solid black;" >Categoría del suceso</th>
<th style="border:1px solid black;" >Origen del suceso</th>
<th style="border:1px solid black;" >Id. de suceso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Lista de revocación de certificados caducada</td>
<td style="border:1px solid black;">No se puede obtener acceso a una lista de revocación de certificados válida, lo que actualmente provoca una pérdida del servicio.</td>
<td style="border:1px solid black;">Error</td>
<td style="border:1px solid black;">Operaciones de la entidad emisora</td>
<td style="border:1px solid black;">20</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Lista de revocación de certificados atrasada</td>
<td style="border:1px solid black;">La lista de revocación de certificados aún es válida, pero existe una lista nueva atrasada que debería haberse publicado.</td>
<td style="border:1px solid black;">Error</td>
<td style="border:1px solid black;">Operaciones de la entidad emisora</td>
<td style="border:1px solid black;">21</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">No se puede recuperar la lista de revocación de certificados de Active Directory</td>
<td style="border:1px solid black;">Una lista de revocación de certificados no se encuentra disponible en un punto de distribución de lista de revocación de certificados publicada. Esto puede originar una pérdida de servicio.</td>
<td style="border:1px solid black;">Error</td>
<td style="border:1px solid black;">Operaciones de la entidad emisora</td>
<td style="border:1px solid black;">22</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Los Servicios de Certificate Server no responden:
Id. de suceso 1: interfaz de cliente sin conexión
Id. de suceso 2: interfaz de administrador sin conexión</td>
<td style="border:1px solid black;">La interfaz de llamadas a procedimiento remoto (RPC) de los Servicios de Certificate Server está sin conexión y los certificados no pueden emitirse. Es posible que sea necesario reiniciar el servicio.</td>
<td style="border:1px solid black;">Error</td>
<td style="border:1px solid black;">Operaciones de la entidad emisora</td>
<td style="border:1px solid black;">1 y
2</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Otros sucesos</td>
<td style="border:1px solid black;">Error en la ejecución de la secuencia de comandos de supervisión de la entidad emisora</td>
<td style="border:1px solid black;">Error</td>
<td style="border:1px solid black;">Operaciones de la entidad emisora</td>
<td style="border:1px solid black;">100</td>
</tr>
</tbody>
</table>
  
#### Administración de cambios
  
Las tareas de esta sección hacen referencia a los cambios que posiblemente necesite para configurar la infraestructura de seguridad de WLAN.
  
##### Administración de actualizaciones de seguridad de Windows
  
Tanto las actualizaciones de IAS como las de los Servicios de Certificate Server están incluidas en los paquetes y revisiones de servicios básicos para Windows Server 2003. No necesita actualizar estos componentes por separado.
  
Debería leer esta guía y seguir las referencias facilitadas en la sección "Actualizaciones de seguridad del servidor" del capítulo 3, "Preparación del entorno".
  
##### Administración de cambios en los servidores IAS
  
En el capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas", se recomendaba designar uno de los servidores IAS como el servidor "maestro", servidor en el que realizaría los cambios en la configuración de IAS (consulte la sección "Implementación de la configuración en varios servidores IAS" del capítulo 5). Estos cambios se replicarían a los otros servidores de la organización mediante exportaciones e importaciones de la base de datos de la configuración de IAS automatizadas; así, se aseguraría la consistencia de la configuración en toda la infraestructura de IAS.
  
No obstante, el conjunto de clientes RADIUS (los puntos de acceso inalámbrico) configurado en cada IAS no se replica normalmente. Los puntos de acceso admitidos por cada servidor pueden variar sustancialmente y raro sería el caso en que dos servidores IAS tuvieran exactamente el mismo conjunto de clientes. Esto puede suceder, por ejemplo, si tiene dos servidores IAS centrales para atender todos los puntos de acceso inalámbrico de la organización.
  
###### Creación de copias de seguridad de la configuración IAS antes de realizar cambios
  
Aunque haya programado copias de seguridad de los servidores para cada noche, resulta muy conveniente realizar una copia de seguridad manual del IAS antes de realizar cambios en los servidores. Esto le permitirá deshacer cualquier cambio y restaurar el estado del servidor a aquél inmediatamente anterior a los cambios realizados. El siguiente procedimiento se sirve de la secuencia de comandos de la creación de copias de seguridad para exportar la configuración del servidor, directivas, la configuración del registro y clientes RADIUS.
  
**Para crear copias de seguridad de la configuración de IAS**
  
1.  Abra un shell de comandos en el servidor utilizando el acceso directo de **MSS WLAN Tools** e introduzca el siguiente comando para crear una carpeta en la que guardar el archivo de exportación de IAS:
  
    **md c:\\IASSaveState**
  
    La configuración de IAS suele ser menor de 100 KB y se puede guardar en la unidad del sistema, tal y como se muestra en el ejemplo. No obstante, se puede utilizar cualquier ruta siempre y cuando se use de forma coherente en este comando y en los posteriores.
  
2.  Utilice el siguiente comando para establecer permisos para la carpeta de forma que sólo los administradores y operadores de copias de seguridad puedan leer y modificar el contenido:
  
    **cacls c:\\IASSaveState /G system:F administrators:F "Backup Operators":C**
  
    Es probable que este comando se divida en varias líneas en este documento, pero debe escribirlo como una sola línea.
  
3.  Para exportar la configuración de IAS, ejecute la secuencia de comandos de creación de copias de seguridad mediante el siguiente comando:
  
    **MSSTools BackupIAS /path:C:\\IASSaveState**
  
###### Replicación de la configuración en otros servidores IAS
  
Debe establecer un procedimiento propio repetitivo para garantizar que la configuración del servidor maestro se replique en el resto de servidores IAS de la organización. Es posible que esto implique ordenar al personal de soporte local que importe la configuración. Lo más normal es que este procedimiento se realice de forma remota copiando los archivos de configuración y utilizando una sesión en el escritorio remoto con el objetivo de ejecutar la secuencia de comandos para importar la configuración.
  
Para replicar la configuración en otros servidores IAS, siga los procedimientos descritos en la sección "Replicación de la configuración desde el servidor IAS principal" del capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas".
  
**Nota:** es probable que encuentre útil incrustar un número de versión en el nombre de la directiva de acceso remoto para que sea fácil comprobar que todos los servidores IAS tienen la misma versión de configuración.
  
##### Adición de servidores IAS al entorno
  
Antes de instalar un nuevo servidor IAS, debe identificar los puntos de acceso inalámbrico que configurará como clientes de este servidor. Para ello, siga las instrucciones facilitadas en el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas". Asimismo, necesitará otro servidor IAS configurado como el servidor RADIUS secundario para proporcionar resistencia a los puntos de acceso en caso de error en el servidor. Si está reconfigurando los puntos de acceso existentes para utilizar este nuevo servidor, deberá planear la migración con detenimiento a fin de evitar trastornos en el servicio para los usuarios durante el cambio de puntos de acceso. Normalmente no se producirán trastornos, siempre y cuando un punto de acceso tenga, al menos, un servidor RADIUS de autenticación activo.
  
**Para instalar IAS en un servidor nuevo**
  
1.  Para preparar el servidor, siga las instrucciones del capítulo 3, "Preparación del entorno".
  
2.  Siga las instrucciones de las secciones "Instalación de IAS" y "Registro de IAS en Active Directory" del capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas".
  
3.  Para replicar los cambios desde el servidor IAS maestro al servidor nuevo, siga el procedimiento descrito en la sección "Replicación de la configuración desde el servidor IAS principal" del capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas".
  
4.  Por último, agregue las entradas de cliente RADIUS para los puntos de acceso a IAS inalámbricos y configure dichos puntos de acceso para utilizar el nuevo servidor IAS.
  
##### Adición de puntos de acceso inalámbrico a la red
  
Para agregar un nuevo punto de acceso inalámbrico, debe completar las dos tareas siguientes:
  
1.  Agregue el punto de acceso como cliente RADIUS al servidor IAS principal y al secundario.
  
2.  Configure el punto de acceso para usar los servidores IAS como servidores RADIUS principal y secundario.
  
Los servidores IAS elegidos como servidores RADIUS principal y secundario dependerán de la ubicación del punto de acceso en la red. Lo ideal es elegir un servidor IAS principal que esté en la misma LAN que el punto de acceso o que tenga, al menos, una conectividad al punto de acceso confiable. Elija un servidor IAS secundario con una conectividad al punto de acceso confiable. Para obtener más información, consulte las instrucciones facilitadas en la sección "Asignación de puntos de acceso a servidores RADIUS" del capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas".
  
Una vez identificados los servidores IAS adecuados para el punto de acceso, lleve a cabo los siguientes procedimientos , que son los mismos descritos para agregar un punto de acceso a IAS en el capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas".
  
**Para agregar un punto de acceso a la red**
  
1.  Para agregar el punto de acceso como cliente RADIUS al IAS principal, siga el procedimiento descrito en la sección "Adición de puntos de acceso al servidor IAS principal" del capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas".
  
2.  Para agregar el punto de acceso como cliente RADIUS al IAS secundario, siga el procedimiento descrito en la sección "Importación de puntos de acceso en el servidor IAS secundario" del capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas".
  
3.  Configure el punto de acceso siguiendo las instrucciones proporcionadas en la sección "Configuración de puntos de acceso inalámbrico" del capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas".
  
##### Eliminación de un punto de acceso inalámbrico
  
Si está volviendo a ubicar y organizar los sitios, es probable que necesite quitar un punto de acceso inalámbrico de la red. Es recomendable quitar siempre del servidor IAS aquellas entradas de cliente RADIUS que ya no estén en uso.
  
**Para quitar un punto de acceso inalámbrico de la red**
  
1.  Identifique los servidores IAS principal y secundario de los que hay que quitar el punto de acceso.
  
2.  Utilice la MMC del **Servicio de autenticación de Internet** para eliminar la entrada del cliente RADIUS del punto de acceso. Compruebe que la IP del cliente RADIUS coincide con la dirección IP del punto de acceso retirado. No tome como referencia el nombre del cliente RADIUS.
  
3.  Repita el paso 2 en el servidor IAS secundario.
  
##### Concesión del acceso a WLAN a un usuario o equipo
  
Si ha seguido la configuración predeterminada de esta solución, todos los usuarios y equipos del dominio en el que haya instalado los servidores IAS tendrán acceso automático a la WLAN. Esto se debe a que los grupos de usuarios y de equipos de dominio son miembros de los grupos de usuarios y de equipos respectivos de la LAN inalámbrica. Estos grupos pertenecen, a su vez, al grupo de acceso a LAN inálambrica, que la directiva de acceso remoto IAS usa para conceder acceso a la WLAN.
  
###### Control del acceso para miembros del mismo dominio
  
Si desea controlar explícitamente qué usuarios y equipos se pueden conectar a la WLAN, deberá recurrir a grupos de seguridad para administrar el acceso. Debe eliminar los grupos de usuarios y equipos de dominio de los respectivos grupos de usuarios y equipos de la LAN inalámbrica para, a continuación, agregar los usuarios y los equipos específicos a los que desee otorgar acceso a WLAN.
  
Si procede de este modo, modificará la configuración predeterminada de la solución, de forma que WLAN se torna inaccesible para todos, a menos que se conceda acceso explícito mediante la adición al grupo de seguridad. Se trata de un enfoque más prudente que el de "permitir de forma predeterminada" y, por lo general, las organizaciones con necesidades de alta seguridad se decantan por él. También puede resultar útil en los casos en los que sólo un número limitado de personas tiene acceso a la WLAN. Un ejemplo podría ser la fase piloto de una instalación mayor.
  
**Para habilitar el acceso a WLAN de un usuario o un equipo en el mismo dominio**
  
1.  Con **Usuarios y equipos de Active Directory**, agregue la cuenta de usuario o de equipo al grupo de usuarios o equipos de LAN inalámbrica.
  
2.  Si está agregando un usuario, pida al usuario que cierre la sesión y la vuelva a iniciar. Si está agregando un equipo, reinícielo.
  
3.  Compruebe que el usuario o el equipo puedan tener acceso a WLAN.
  
###### Control del acceso para miembros de otro dominio
  
Si tiene un bosque con varios dominios, es probable que desee permitir que usuarios y equipos de otros dominios utilicen la WLAN. Para ello, necesita iniciar sesión utilizando una de las cuentas siguientes:
  
-   Un administrador de ambos dominios.
  
-   Una cuenta con permisos para crear grupos en otros dominios y para modificar los miembros del grupo de acceso a WLAN en el dominio principal; es decir, el dominio en el que están instalados los servidores IAS.
  
**Para conceder acceso a WLAN a los usuarios y equipos de otros dominios**
  
1.  Inicie sesión con una cuenta que tenga permisos para crear grupos en el dominio al que pertenecen los usuarios y equipos a los que quiere conceder acceso a WLAN (el dominio de destino).
  
2.  Abra **Usuarios y equipos de Active Directory** y céntrese en un controlador de dominio para el dominio de destino.
  
3.  Cree un grupo global de dominio llamado Usuarios de LAN inalámbrica en el dominio de destino.
  
4.  Cree un grupo global de dominio llamado Equipos de LAN inalámbrica en el dominio de destino.
  
5.  Inicie sesión con una cuenta que tenga permisos para modificar la pertenencia al grupo de acceso a LAN inalámbrica en el dominio principal. Con **Usuarios y equipos de Active Directory**, busque el grupo de acceso a LAN inalámbrica y ábralo para modificar sus propiedades. Desde la ficha **Pertenencia** de las propiedades del grupo, agregue desde el dominio de destino los grupos Usuarios de LAN inalámbrica y Equipos de LAN inalámbrica como miembros de este grupo.
  
6.  Identifique a los usuarios del dominio de destino que requieren acceso a WLAN. Agregue sus cuentas al grupo Usuarios de LAN inalámbrica de ese dominio. Del mismo modo, agregue las cuentas de equipos necesarias del dominio de destino al grupo Equipos de LAN inalámbrica de dicho dominio. Otra forma consiste en agregar a los Usuarios del dominio y Equipos del dominio a estos grupos para conceder acceso a WLAN a todos los miembros del dominio de destino.
  
##### Denegación del acceso a WLAN a un usuario o equipo
  
La configuración predeterminada de esta solución concede acceso a WLAN a todos los usuarios y equipos del dominio en el que se han instalado los servidores IAS. Este acceso se concede automáticamente porque son miembros de los grupos Usuarios del dominio y Equipos del dominio respectivamente. Esto puede acarrear problemas si necesita bloquear el acceso a WLAN para usuarios o equipos individuales. No debe quitar usuarios o equipos de los grupos de Usuarios del dominio y Equipos del dominio integrados; en vez de ello, utilice una de las siguientes estrategias:
  
-   Si el usuario ha dejado la organización (o, en el caso de un equipo, si se ha perdido o lo han robado), puede deshabilitar la cuenta de dicho usuario o equipo en Active Directory.
  
-   Administre el acceso mediante los permisos de acceso remoto en el objeto de cuenta de usuario o de equipo para permitir o denegar el acceso. Esto se ha analizado brevemente en la sección "Acceso de los usuarios y los equipos a la WLAN" del capítulo 6, "Configuración de clientes de LAN inalámbricas".
  
-   Si desea eliminar el acceso a WLAN de un usuario o equipo pero seguir permitiendo que la cuenta se utilice para el acceso normal al dominio o a otras redes, tendrá que utilizar un modelo WLAN de acceso selectivo, o bien implementar una directiva de acceso remoto "Denegar". La opción elegida dependerá de si desea que el acceso a WLAN se conceda de forma predeterminada, o bien que se deniegue de forma predeterminada y que se conceda sólo a los usuarios especificados.
  
    -   El uso de la pertenencia a un grupo específico para implementar una directiva de acceso selectivo ya se ha descrito anteriormente en el capítulo, en el procedimiento "Concesión del acceso a WLAN a un usuario o equipo". Puede denegar el acceso a WLAN sólo con quitar a un usuario o equipo del grupo de seguridad pertinente.
  
    -   El siguiente procedimiento, "Control del acceso a WLAN mediante una directiva de denegación", describe la creación de una directiva de acceso remoto de IAS para denegar el acceso a los grupos seleccionados.
  
        **Importante:** no debe quitar usuarios o equipos de los grupos Usuarios del Dominio o Equipos del dominio respectivamente. Aunque técnicamente es posible, si lo hace impedirá que la cuenta de usuario o equipo funcione correctamente en el uso normal del dominio.
  
###### Control del acceso a WLAN mediante una directiva de denegación
  
Si desea permitir el acceso de forma predeterminada, pero poder denegarlo a usuarios y equipos individuales como excepción, habrá de crear una directiva de acceso remoto "Denegar" en IAS.
  
**Para crear una directiva de acceso remoto de denegación**
  
1.  En **Usuarios y equipos de Active Directory**, cree un grupo universal llamado Denegar acceso a LAN inalámbrica.
  
2.  Cree los grupos globales de dominio Denegar usuarios de LAN inalámbrica y Denegar equipos de LAN inalámbrica y agréguelos como miembros del grupo Denegar acceso a LAN inalámbrica.
  
3.  Inicie sesión en el servidor IAS maestro que utiliza para editar la configuración de IAS global, configuración que se replicará más tarde en los otros servidores IAS.
  
4.  En la MMC del **Servicio de autenticación de Internet**, haga clic con el botón secundario en la carpeta **Directivas de acceso remoto** y seleccione **Nueva directiva de acceso remoto**.
  
5.  Seleccione **Configurar una directiva personalizada** y escriba **Denegar acceso a LAN inalámbrica** como nombre de la directiva. Haga clic en **Siguiente** para continuar.
  
6.  Haga clic en **Agregar** para agregar una condición de directiva. Seleccione **Grupos de Windows** de la lista y haga clic en **Agregar**.
  
7.  Haga clic en **Agregar** para agregar un grupo de seguridad. Escriba (o busque) el grupo Denegar acceso a LAN inalámbrica y haga clic en **Aceptar**.
  
8.  Haga clic en **Agregar** para agregar condición de directiva distinta. Seleccione **Tipo de puerto NAS** de la lista y haga clic en **Agregar**.
  
9.  De la lista de **Tipos disponibles**, seleccione **Inalámbrica - IEEE 802.11** y haga clic en **Agregar &gt;&gt;**. A continuación, seleccione **Inalámbrica - Otra** y haga clic en **Agregar &gt;&gt;** para agregarlas a la lista **Tipos seleccionados**. Haga clic en **Aceptar** para concluir y en **Siguiente** para continuar.
  
10. Seleccione **Denegar permiso de acceso remoto** y haga clic en **Siguiente** para continuar.
  
11. En la pantalla **Perfil**, haga clic en **Siguiente** para omitirla y, a continuación, haga clic en **Finalizar** para concluir.
  
12. La directiva **Denegar acceso a LAN inalámbrica** se debe crear al principio de la lista de directivas como prioridad más alta o, al menos, por encima de la directiva Permitir acceso a LAN inalámbrica. Si no es así, haga clic con el botón secundario en el nombre de la directiva y haga clic en **Subir** hasta que ocupe un lugar anterior en la lista al de la directiva **Permitir acceso a LAN inalámbrica**.
  
13. Utilice los procedimientos descritos anteriormente para replicar la nueva configuración en los otros servidores IAS de la organización.
  
Se rechazará el acceso a WLAN a todo usuario o equipo que agregue a los grupos Denegar usuarios de LAN inalámbrica o Denegar equipos de LAN inalámbrica. No obstante, esta configuración sólo surtirá efecto la próxima vez que inicie sesión el usuario denegado o cuando se reinicie el equipo denegado.
  
#### Tareas de soporte técnico
  
Esta sección cubre las tareas más comunes que necesita realizar para solucionar los problemas en la infraestructura de seguridad de WLAN. La sección "Solución de problemas" de este capítulo hace referencia a muchas de estas tareas.
  
##### Restauración de la configuración de un servidor IAS a partir de copias de seguridad
  
Las directivas y configuración de IAS se almacenan en la base de datos de configuración de IAS. Éstas se pueden restaurar independientemente del resto de la configuración del sistema. Debe programar la tarea de creación de copias de seguridad de IAS para realizar estas copias cada noche en la carpeta C:\\IASBackup. Para obtener más información sobre este tema, consulte el procedimiento "Configuración de la copia de seguridad de IAS" en la sección "Tareas operativas" de este capítulo. Si ha de deshacer los cambios aplicados ese día, puede restaurar la configuración a partir de los archivos de las copias de seguridad (en C:\\IASBackup) creados la noche anterior, o a partir de la copia de seguridad de reversión realizada antes de hacer los cambios. Para obtener más detalles, consulte el procedimiento "Creación de copias de seguridad de la configuración IAS antes de realizar cambios" en la sección "Administración de cambios".
  
Si necesita restaurar una versión anterior de la configuración, ha de recuperar de la copia de seguridad del servidor la configuración de IAS exportada.
  
**Advertencia:** este procedimiento restaurará la configuración de IAS completa (incluidos los clientes RADIUS) y sobrescribirá la configuración existente en el servidor. La copia de seguridad que intenta restaurar debe provenir del mismo servidor.
  
**Para restaurar la configuración de IAS**
  
1.  Si los archivos de copia de seguridad de la configuración de IAS que desea utilizar no se encuentran en el servidor, deberá restaurarlos a partir de medios de copia de seguridad. Asegúrese de seleccionar en la carpeta IASBackup sólo los archivos que hay que restaurar. No restaure el estado del sistema, a no ser que también desee revertir a una configuración del sistema anterior.
  
2.  Utilice el acceso directo **MSS WLAN Tools** para abrir un shell de comandos. Para restaurar la configuración de IAS, ejecute el siguiente comando:
  
    **msstools RestoreIAS /path:C:\\IASBackup**
  
3.  Para comprobar que la configuración de IAS se ha restaurado, abra la consola de administración de IAS y compruebe los clientes RADIUS y las carpetas de directivas de acceso remoto.
  
Si, por cualquier razón, no dispone de ninguna copia de seguridad de este sistema utilizable, puede exportar la configuración desde otro servidor IAS e importarla a éste. Normalmente, los servidores IAS con la misma función comparten los mismos valores de configuración, pero cuentan con un conjunto distinto de clientes RADIUS. Por esta razón, no debe utilizar este procedimiento para restaurar la configuración desde otro servidor. En su lugar, recurra al procedimiento "Replicación de la configuración desde el servidor IAS principal" del capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas".
  
**Importante:** debe asegurarse de que el sistema restaurado está actualizado, ya que, dado que se ha restaurado a partir de una copia de seguridad antigua, puede que las revisiones previamente aplicadas se hayan deshecho.
  
##### Restauración de la configuración completa del servidor a partir de copias de seguridad
  
Los procedimientos para restaurar el servidor variarán en función del sistema de copia de seguridad elegido. Los procedimientos que siguen se basan en el supuesto de que ha realizado la copia de seguridad del sistema mediante la creación de una copia de seguridad del estado del sistema de Windows en un archivo, seguida de una copia de seguridad de este archivo y de otros archivos necesarios.
  
**Para restaurar el servidor**
  
1.  Según sea el estado del servidor, es posible que necesite preparar el servidor desde el principio, y así, cuando un error grave del hardware ha destruido los discos de sistema del servidor. Si no es el caso, puede realizar la restauración directamente sin reinstalar el sistema operativo.
  
2.  En caso de usar copias de seguridad del estado del sistema y de los archivos por separado, utilice el software de copias de seguridad para restaurar los archivos de las copias de seguridad del estado del sistema y los de la configuración de IAS desde el medio de copia de seguridad al servidor. La configuración de IAS se debe restaurar en la misma ruta, que es C:\\IASBackup.
  
3.  Ejecute la utilidad de copias de seguridad de Windows y seleccione el archivo de la copia de seguridad del estado del sistema restaurado. Deberá pertenecer a un grupo que posea derechos de creación de copias de seguridad y restauración en el equipo (como Operadores de copia de seguridad o Administradores).
  
4.  Haga clic en **Restaurar**.
  
5.  Reinicie el sistema.
  
6.  Compruebe que todo funciona según lo esperado y que Active Directory y los Servicios de Certificate Server, si se han instalado, se han iniciado sin errores.
  
7.  Utilice el acceso directo **MSS WLANTools** para abrir un shell de comandos. Para restaurar la configuración de IAS, ejecute el siguiente comando:
  
    **MSSTools RestoreIAS /path:C:\\IASBackup**
  
8.  Para comprobar que la configuración de IAS se ha restaurado, abra la consola de administración de IAS y compruebe los clientes RADIUS y las carpetas de directivas de acceso remoto.
  
    **Importante:** si IAS se está ejecutando en un controlador de dominio, al restaurar una copia de seguridad del estado del sistema, se restaurará en ese servidor la versión de la base de datos de Active Directory de la que se había realizado una copia de seguridad. No obstante, todo cambio realizado en Active Directory con posterioridad a la copia de seguridad se replicará en el servidor restaurado en el siguiente ciclo de replicación de Active Directory.
  
#### Tareas de optimización
  
Esta sección cubre las tareas relevantes para optimizar la ejecución de la infraestructura de IAS.
  
##### Determinación de la carga máxima del servidor IAS
  
En esta sección se ofrece información sobre la posible carga máxima del servidor IAS.
  
Los problemas de rendimiento en servidores IAS con la configuración y el tamaño correctos son muy poco frecuentes. Los servidores IAS se encuentran bajo una mayor carga durante horas de mayor demanda como, por ejemplo, las mañanas (cuando muchos usuarios inician la sesión a la vez), poco después de una interrupción de la actividad de la red, o bien cuando se produce un error del servidor RADIUS en el que los puntos de acceso inalámbrico conmutan por error a un servidor de copia de seguridad.
  
La siguiente tabla recoge indicaciones de los requisitos de autenticación WLAN para diversos tamaños de organización.
  
**Tabla 8.7. Requisitos de autenticación WLAN**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Número de usuarios de WLAN</th>
<th style="border:1px solid black;" >Nuevas autenticaciones por segundo</th>
<th style="border:1px solid black;" >Nuevas autenticaciones por segundo en hora máxima</th>
<th style="border:1px solid black;" >Reautenticaciones por segundo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">100</td>
<td style="border:1px solid black;">&gt; 0,1</td>
<td style="border:1px solid black;">0,1</td>
<td style="border:1px solid black;">0,1</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">1000</td>
<td style="border:1px solid black;">0,1</td>
<td style="border:1px solid black;">0,6</td>
<td style="border:1px solid black;">1,1</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">10.000</td>
<td style="border:1px solid black;">1,4</td>
<td style="border:1px solid black;">5,6</td>
<td style="border:1px solid black;">11,1</td>
</tr>
</tbody>
</table>
  
La columna Nuevas autenticaciones por segundo forma parte de la carga fija; en ella, se supone una media de cuatro autenticaciones nuevas completas, dado que los usuarios se desplazan por los puntos de acceso inalámbrico. La columna Nuevas autenticaciones por segundo en hora máxima señala el tipo de carga que se espera cuando todos los usuarios se deben autenticar en un período de 30 minutos (por ejemplo, al inicio del día). La columna Reautenticaciones por segundo contempla el número de autenticaciones con reconexiones rápidas que tienen lugar cuando IAS obliga a establecer un tiempo de espera de sesión transcurridos 15 minutos. Aunque el tiempo de espera predeterminado en la solución es de 60 minutos, se usa la opción de 15 minutos para ponerse en el peor de los casos. Debe evaluar estas cifras frente a las necesidades de su propia organización para determinar qué tipo de carga necesita admitir.
  
Las pruebas internas realizadas por Microsoft muestran que IAS puede admitir una carga elevada con un hardware modesto. La carga admitida por IAS se representa mejor con el número de autenticaciones Protocolo de autenticación extensible (EAP) por segundo. La tabla siguiente contempla los resultados de un servidor IAS ejecutado en un servidor Intel Pentium 4 a 2GHz con Windows Server 2003.
  
Las pruebas se llevaron a cabo con el registro de RADIUS activado (en un disco aparte) y con IAS en un servidor distinto al del controlador de dominio de Active Directory. Por tanto, estas cifras se deben considerar como el peor de los casos. La configuración predeterminada de esta solución presenta el registro desactivado e IAS instalado en el mismo servidor que el controlador de dominio. Ambos elementos mejorarán el rendimiento de la autenticación.
  
**Nota:** esta información se ofrece sin garantía alguna de exactitud y sólo se debe utilizar como orientación con objeto de planear la capacidad y no para realizar comparaciones de rendimiento.
  
**Tabla 8.8. Ejemplo de medidas de la capacidad del servidor IAS**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Tipo de autenticación</th>
<th style="border:1px solid black;" >Autenticaciones por segundo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Nuevas autenticaciones con el nuevo protocolo de autenticación extensible protegido (PEAP)</td>
<td style="border:1px solid black;">36</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Nuevas autenticaciones PEAP con compatibilidad para tarjetas de descarga de TLS/SSL</td>
<td style="border:1px solid black;">50</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Autenticaciones con reconexión rápida</td>
<td style="border:1px solid black;">166</td>
</tr>
</tbody>
</table>
  
IAS se puede configurar para generar registros de RADIUS basados en el disco que contengan diversos volúmenes de información sobre solicitudes de RADIUS. Si opta por activar el registro de RADIUS, tendrá que considerar los costes generales que supondrá para los servidores, sobre todo, en los subsistemas de discos. El bajo rendimiento del disco actuará como un cuello de botella para el rendimiento de IAS y retrasará las repuestas RADIUS de IAS a los puntos de acceso. Esto conducirá a tiempos de espera del protocolo y a conmutaciones innecesarias de puntos de acceso en servidores RADIUS secundarios. Si espera una carga elevada (puede utilizar las cifras de las tablas anteriores como orientación) y va a activar el registro de RADIUS, se debe asegurar de que IAS está configurado para escribir registros RADIUS en un disco de alto rendimiento distinto del de la unidad del sistema de Windows y del de los archivos de paginación.
  
La habilitación de las características de seguimiento en IAS de Windows Server 2003 (como se describe en la sección "Habilitación y deshabilitación del seguimiento en el servidor IAS" de este capítulo) también generará carga adicional en los servidores IAS. Estas características pueden ser necesarias de vez en cuando para solucionar problemas relacionados con el acceso a la red, pero no deberían estar habilitadas de forma permanente. No obstante, es posible que desee asegurarse de que los servidores IAS disponen de algún espacio adicional para permitir el seguimiento durante períodos de tiempo determinados y seguir atendiendo la carga de producción.
  
##### Otras medidas de optimización
  
Para obtener más información sobre la optimización de IAS, consulte la sección sobre el diseño de una solución de IAS optimizada en el capítulo dedicado a la implementación de IAS del *Kit de distribución de Microsoft Windows Server 2003*.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Solución de problemas
  
Esta sección contiene procedimientos y técnicas que ayudan a diagnosticar y solucionar problemas relacionados con la solución de LAN inalámbrica.
  
#### Procedimientos para la solución de problemas
  
Los siguientes procedimientos facilitan la identificación de las posibles causas de un problema y la acción necesaria para resolverlo. Esta sección se organiza de forma jerárquica. El primer procedimiento, "Determinación del tipo de problema", le indicará uno de varios procedimientos, cada uno de los cuales se desglosa en pasos detallados para la solución del problema. Estos procedimientos, a su vez, pueden apuntar hacia otros procedimientos centrados en un componente particular de la solución.
  
Cada uno de estos procedimientos se describe en detalle más adelante en este mismo capítulo. Algunos de ellos se presentan en forma gráfica; otros aparecen en tablas o texto por exigir una descripción demasiado extensa para una figura. Alguno de estos procedimientos recurre a la sección "Herramientas y técnicas para la solución de problemas" de este capítulo. Se debe familiarizar con dicha sección para utilizar estos procedimientos de forma eficaz.
  
**Importante:** estos procedimientos de diagnóstico no cubren todos los casos. En aquellos casos en los que los pasos de investigación recomendados no le conduzcan al origen del problema, debe volver hacia atrás y seguir otro de los procedimientos de diagnóstico. En algunas ocasiones, no advertirá el alcance completo o la naturaleza de los síntomas, lo que puede conducirle por el camino erróneo. Por ejemplo, es posible que un usuario sea la única persona de una oficina encargada de comunicar un problema que afecta a toda la oficina. Aunque la tabla indique los procedimientos de diagnóstico relacionados con los errores de un único cliente, es probable que otros procedimientos sean más adecuados.
  
Además, debe consultar los documentos sobre la solución de problemas en WLAN e IAS enumerados al término del capítulo.
  
##### Determinación del tipo de problema
  
Comience por clasificar el tipo de problema que ha surgido con ayuda del diagrama de flujo siguiente. Los rombos representan preguntas o puntos de decisión, mientras que los rectángulos muestran el diagnóstico del problema e indican el nombre del procedimiento que hay que seguir.
  
![](images/Dd162271.PEAP_801(es-es,TechNet.10).gif)
  
**Figura 8.1. Determinación del tipo de problema**
  
##### Diagnóstico de los problemas de conexión del cliente
  
La siguiente tabla clasifica los distintos tipos de problemas de conexión basados en el número y en la ubicación de los clientes afectados. La columna Posible(s) problema(s) refleja los factores que pueden producir los síntomas señalados con mayor probabilidad. La columna Procedimientos de diagnóstico que seguir contiene los procedimientos de diagnóstico a los que debe recurrir en primer lugar para diagnosticar el problema. Más adelante podrá encontrar una descripción detallada de cada uno de estos procedimientos.
  
**Tabla 8.9. ¿Quién no puede conectarse a la WLAN?**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Síntoma</th>
<th style="border:1px solid black;" >Posible(s) problema(s)</th>
<th style="border:1px solid black;" >Procedimientos de diagnóstico que seguir</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Un único cliente</td>
<td style="border:1px solid black;">Configuración del equipo o cuenta del usuario/equipo</td>
<td style="border:1px solid black;">Comprobar cuenta de usuario/equipo
Comprobar el equipo cliente</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Varios clientes en un sitio</td>
<td style="border:1px solid black;">Configuración incorrecta de uno o varios puntos de acceso</td>
<td style="border:1px solid black;">Comprobar configuración de puntos de acceso inalámbrico</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Todo un sitio (IAS local)</td>
<td style="border:1px solid black;">Funcionamiento o configuración incorrecta del servidor IAS en este sitio; problemas de replicación en Active Directory que impiden al controlador de dominio recibir información correcta; funcionamiento incorrecto del servidor IAS asociados a problemas de conectividad de WLAN.</td>
<td style="border:1px solid black;">Comprobar Active Directory y Servicios de red
Comprobar IAS
Comprobar conectividad WAN</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Todo un sitio (IAS no local)</td>
<td style="border:1px solid black;">Problemas de conectividad con WLAN; problemas de replicación en Active Directory (si se trata del controlador de dominio local).</td>
<td style="border:1px solid black;">Comprobar conectividad WAN</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Todos los clientes en todos los sitios</td>
<td style="border:1px solid black;">Configuración de la organización (objeto de directiva de grupo de la configuración del cliente, grupos con la directiva de acceso remoto, errores en la renovación de certificados).</td>
<td style="border:1px solid black;">Comprobar Active Directory y Servicios de red (comprobaciones &quot;Comprobar objetos de directiva de grupo de la configuración de WLAN y &quot;Comprobar grupos de Active Directory&quot;).
Comprobar la entidad emisora de certificados
Comprobar IAS</td>
</tr>
</tbody>
</table>
 

##### Diagnóstico de los problemas de rendimiento

Esta sección se centra en los problemas de rendimiento asociados con la infraestructura de seguridad de WLAN. En este capítulo no se tratan los problemas generales de rendimiento de la red inalámbrica y con cable.

**Tabla 8.10. Problemas de rendimiento**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Síntoma</th>
<th style="border:1px solid black;" >Posible solución</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Demora en la autenticación que afecta a muchos usuarios</td>
<td style="border:1px solid black;">El servidor IAS está muy cargado, compruebe el monitor de rendimiento.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Autenticación a través de un vínculo WLAN lento (incluso si un IAS local ha comprobado que los puntos de acceso no han producido errores al conectarse con el IAS remoto).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Las demoras con un servidor Protocolo de configuración dinámica de host (DHCP) al emitir una dirección IP puede afectar al tiempo total de conexión.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Demora en la reautenticación mientras se desplaza entre puntos de acceso</td>
<td style="border:1px solid black;">Un retraso de pocos segundos es normal cuando se cambia de punto de acceso.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Si un cliente se sale del alcance de un punto de acceso (y permanece fuera más de 10 segundos), puede necesitar hasta 60 segundos para que se inicie la reautenticación una vez vuelva a hallarse al alcance de un punto de acceso. Esto ocurre porque, al desconectarse de una WLAN, el cliente WLAN con Windows sólo busca las WLAN disponibles cada 60 segundos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">El rendimiento de la red WLAN es bajo</td>
<td style="border:1px solid black;">El origen de este síntoma puede ser la existencia de demasiados clientes que utilizan pocos puntos de acceso, la colocación incorrecta de los puntos de acceso o señales de radio débiles debido a la obstrucción o a una distancia excesiva.
Todos estos aspectos pertenecen al diseño de la red WLAN y se encuentran fuera del alcance de este documento. Para recibir algún tipo de consejo, debe consultar a su proveedor o al proveedor de la solución.
Para obtener más información, consulte el capítulo sobre la implementación de LAN inalámbricas del <em>Kit de distribución de Microsoft Windows Server 2003</em>.</td>
</tr>
</tbody>
</table>
 

##### Se autentica al cliente, pero el equipo da error

Esta solución recurre a la autenticación tanto del usuario como del equipo a la WLAN. Las credenciales de dominio del equipo se utilizan para autenticar a la WLAN cuando ningún usuario ha iniciado sesión en el equipo. Cuando un usuario inicia sesión, se utilizan las credenciales de éste para volver a autenticar a la WLAN. Este mecanismo hace posible que el equipo se comunique con la WLAN incluso cuando nadie haya iniciado sesión, al tiempo que permite administrar el equipo de forma remota, descargar la configuración de los objetos de directiva de grupo del servidor, etc.

Cuando un usuario inicia sesión en un equipo WLAN, se produce una pequeña demora mientras el usuario se autentica a la WLAN. Hasta que el usuario está debidamente autorizado para conectarse, la sesión WLAN autenticada del equipo aún se encuentra activa. No obstante, si el equipo no se pudo autenticar, esta demora significa que no existe conectividad con la red al comienzo del inicio de sesión del usuario.

Esto puede originar una serie de problemas delicados. Por ejemplo, no se cargarán los perfiles de itinerancia del usuario, no se aplicarán algunas configuraciones de objetos de directiva de grupo y no se implementarán las secuencias de comandos de inicio de sesión del usuario ni el software basado en objetos de directiva de grupo (ambos elementos se ejecutan muy pronto en el proceso de inicio de sesión).

Para determinar el origen del error en la autenticación del equipo, debe seguir el procedimiento "Comprobar cuenta de usuario/equipo" descrito más adelante en esta guía.

##### Se autentica al equipo, pero el usuario da error

A diferencia del caso anterior, este problema se percibe inmediatamente y se pondrá en conocimiento de los usuarios afectados de inmediato. Para determinar el origen del error en la autenticación del usuario, debe seguir el procedimiento "Comprobar cuenta de usuario/equipo".

##### Procedimientos de diagnóstico

La siguiente sección ofrece una serie de pasos detallados para la solución de problemas a los que se ha hecho mención en secciones anteriores.

###### Comprobar cuenta de usuario/equipo

El siguiente diagrama de flujo le ayudará a diagnosticar la causa de un error en la autenticación de usuarios o equipos.

**Nota:** el cuadro con forma de flecha del diagrama de flujo indica que debería consultar el procedimiento "Comprobar el equipo cliente", tal y como se especifica en el cuadro.

[![](images/Dd162271.PEAP_802(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_802_big(es-es,technet.10).gif)

**Figura 8.2. Comprobación de la cuenta del usuario o equipo**

###### Comprobar el equipo cliente

El siguiente diagrama de flujo ayuda a diagnosticar los problemas con el equipo cliente.

[![](images/Dd162271.PEAP_803(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_803_big(es-es,technet.10).gif)

**Figura 8.3. Comprobación del equipo cliente**

**Nota:** el cuadro con forma de flecha del diagrama de flujo es un vínculo desde el procedimiento "Comprobar cuenta de usuario/equipo".

El estado de la tarjeta de WLAN (tal y como requiere el paso "Deshabilite/habilite la tarjeta de WLAN y observe el estado" mostrado en el diagrama de flujo) se puede consultar en el panel **Detalles** de la carpeta Conexiones de red (en el **Panel de control**). Cuando habilite la tarjeta, deberá comprobar su estado por medio de las siguientes fases:

-   Conexión

-   Autenticación

-   Adquisición de la dirección IP (a no ser que se asigne estáticamente)

La supervisión del punto en el que surgen errores en el proceso constituye uno de los procedimientos de diagnóstico más útiles.

###### Comprobar IAS

La siguiente tabla recoge una serie de comprobaciones que se deben realizar si sospecha que un servidor IAS es origen de problemas.

**Tabla 8.11. Comprobaciones para el diagnóstico de IAS**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Comprobaciones</th>
<th style="border:1px solid black;" >Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">IAS está en ejecución</td>
<td style="border:1px solid black;">Abra la MMC de <strong>Administración de equipos</strong> y desplácese a <strong>Servicios</strong>. Asegúrese de que IAS se encuentra en estado de ejecución.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Configuración de red básica de IAS</td>
<td style="border:1px solid black;">Ejecute el comando <strong>netdiag</strong> para comprobar si existe algún error en la configuración de red del servidor IAS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">El servidor IAS dispone de un certificado de servidor actual</td>
<td style="border:1px solid black;">Abra la MMC <strong>Certificados</strong> y mire en carpeta \Certificados (equipo local)\Personal\Certificados. En esta carpeta, debe encontrar un certificado para el servidor con las siguientes características:
-La fecha actual se encuentra dentro del período de validez del certificado.
-El nombre alternativo del sujeto coincide con el Sistema de nombres de dominio (DNS) del servidor.
-La autenticación del servidor está presente en el Uso de clave extendida.
-El emisor del certificado es de confianza (en la ficha <strong>Ruta confiable</strong>).
-El certificado no se ha revocado.
Consulte la configuración del perfil de la directiva de acceso remoto a IAS, haga clic en la ficha <strong>Autenticación</strong> y consulte la configuración de 802.1X. El certificado del servidor que se acaba de describir debe estar seleccionado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">IAS es miembro del grupo Servidores RAS e IAS del dominio</td>
<td style="border:1px solid black;">El servidor necesita ser miembro de este grupo, al que normalmente se agrega cuando IAS se registra en Active Directory.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">La directiva de acceso remoto a IAS o la directiva de solicitud de conexión es incorrecta</td>
<td style="border:1px solid black;">Compruebe que la configuración de la directiva (y el número de versión, si lo ha incluido) coincide con lo previsto. Si duda, vuelva a implementar la configuración desde el IAS &quot;maestro&quot;.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Consulte los sucesos IAS en el registro de sucesos del sistema</td>
<td style="border:1px solid black;">Compruebe el registro de sucesos del sistema para comprobar si existe algún suceso de advertencia o de error de IAS. Los errores de autenticación no presentan ningún código de motivo que indique el origen del problema.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Habilite el seguimiento en IAS</td>
<td style="border:1px solid black;">Consulte el procedimiento &quot;Habilitación y deshabilitación del seguimiento en el servidor IAS&quot; en la sección &quot;Herramientas y técnicas para la solución de problemas&quot; de este capítulo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Habilite el seguimiento del cliente</td>
<td style="border:1px solid black;">Consulte el procedimiento &quot;Habilitación y deshabilitación del seguimiento en el equipo cliente&quot; en la sección &quot;Herramientas y técnicas para la solución de problemas&quot; de este capítulo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Habilite el registro SChannel</td>
<td style="border:1px solid black;">Para diagnosticar problemas de TLS y los relativos al certificado, habilite el registro SChannel. Para obtener más información, consulte el procedimiento &quot;Habilitación del registro SChannel en el servidor IAS&quot; en la sección &quot;Herramientas y técnicas para la solución de problemas&quot; de este capítulo. También puede habilitar este registro en el equipo cliente para obtener información adicional sobre el diagnóstico desde la perspectiva del cliente.</td>
</tr>
</tbody>
</table>
  
###### Comprobar la entidad emisora de certificados
  
La tabla siguiente contiene una serie de comprobaciones que puede poner en práctica para determinar si el rendimiento de la entidad emisora de certificados es correcto.
  
**Tabla 8.12. Comprobaciones para el diagnóstico de la entidad emisora**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Comprobación</th>
<th style="border:1px solid black;" >Detalle</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Los Servicios de Certificate Server están en ejecución</td>
<td style="border:1px solid black;">Abra la MMC de <strong>Administración de equipos</strong> y desplácese a <strong>Servicios</strong>. Asegúrese de que los Servicios de Certificate Server están en ejecución.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Compruebe la lista de revocación de certificados, si TLS da error (lo cual aparece en el registro de seguimiento RASTLS o en el registro Schannel) o si la entidad emisora no emite certificados.</td>
<td style="border:1px solid black;">Ejecute el comando <strong>msstools CheckCA</strong> en la entidad emisora de certificados para comprobar que existe una lista de revocación de certificados actual publicada y que es accesible.
Si encuentra problemas en servidores IAS particulares (o en sitios concretos), consiga la herramienta de estado de infraestructura de claves públicas (del <em>Kit de recursos de Windows Server 2003</em>). Se trata de una herramienta de la MMC que le mostrará si el servidor encuentra algún problema en el acceso a una lista de revocación de certificados actual o a un certificado de la entidad emisora de certificados.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Si no se ha inscrito ni renovado ningún certificado, consulte el objeto de directiva de grupo de la inscripción automática de certificados.</td>
<td style="border:1px solid black;">-Compruebe que el objeto de directiva de grupo de inscripción automática está vinculado a la ubicación correcta, normalmente el dominio.
-Compruebe que el objeto de directiva de grupo tiene la plantilla &quot;Equipo&quot; establecida como el tipo de certificado que ha de inscribir (en Configuración del equipo\Configuración de Windows\Configuración de seguridad\Directivas de claves públicas\Configuración de la solicitud de certificados automática).
-Compruebe que el grupo de servidores RAS e IAS dispone de permisos en el objeto de directiva de grupo para <strong>Aplicar directiva y lectura</strong> y que no los anula ningún permiso para denegar (por ejemplo, Usuarios autenticados: denegar lectura).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Plantillas de certificados</td>
<td style="border:1px solid black;">La plantilla Equipo se debe asignar a la entidad emisora (compruebe la carpeta de plantillas en la MMC de la <strong>Entidad emisora de certificados</strong>).
La plantilla Equipo debe disponer de <strong>permiso para inscribir al grupo Servidores RAS e IAS</strong> (compruebe que ningún permiso para denegar lo anula).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Interfaz de DCOM de entidad emisora de forma remota</td>
<td style="border:1px solid black;">Ejecute el comando siguiente desde un servidor IAS remoto para comprobar que DCOM/RPC está funcionando entre el servidor y la entidad emisora de certificados.
<strong>certutil -ping-config</strong> <em>NombredeHostdeEntidadEmisora</em><strong>\</strong><em>NombredeEntidadEmisora</em>
donde <em>NombredeHostdeEntidadEmisora</em> es el nombre del equipo del servidor de la entidad emisora y
<em>NombredeEntidadEmisora</em> es el nombre descriptivo asignado a la entidad emisora de certificados cuando se configura (será el nombre que aparezca en <strong>Emitido por:</strong> de la ficha <strong>General</strong> de cualquier certificado emitido por esta entidad).</td>
</tr>
</tbody>
</table>
 

###### Comprobar Active Directory y Servicios de red

La tabla siguiente enumera una serie de comprobaciones que ha de realizar en Active Directory y en otros componentes de red para determinar si están funcionando adecuadamente.

**Tabla 8.13. Comprobaciones para el diagnóstico de Active Directory**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Comprobación</th>
<th style="border:1px solid black;" >Detalle</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Compruebe la comunicación con Active Directory desde IA</td>
<td style="border:1px solid black;">Ejecute el comando <strong>netdiag /test:ldap /test:trust</strong> en el servidor IAS. Este comando también comprobará la existencia de problemas de DNS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Compruebe los grupos de seguridad de WLAN</td>
<td style="border:1px solid black;">Compruebe la pertenencia a los grupos de seguridad utilizados en esta solución para controlar el acceso a WLAN. La pertenencia predeterminada se contempla en la sección &quot;Creación de grupos de seguridad&quot; del capítulo 3, &quot;Preparación del entorno&quot;.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Compruebe el objeto de directiva de grupo de la configuración de WLAN del equipo cliente</td>
<td style="border:1px solid black;">Compruebe que los valores del objeto de directiva de grupo de la configuración de WLAN son correctos, que el objeto de directiva de grupo está vinculado a la unidad organizativa adecuada (o dominio), y que se le han aplicado los permisos correctos. Consulte la sección &quot;Creación de objetos de directiva de grupo de la configuración de WLAN&quot; del capítulo 6, &quot;Configuración de clientes de LAN inalámbricas&quot;.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Compruebe que Active Directory está replicando de forma adecuada</td>
<td style="border:1px solid black;">Ejecute el comando <strong>dcdiag /test:replications</strong> desde el servidor IAS en el que ha encontrado problemas. Incluso si IAS no se está ejecutando en un controlador de dominio, la herramienta dcdiag comprobará también el controlador de dominio utilizado por dicho servidor IAS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Compruebe el servidor DHCP</td>
<td style="border:1px solid black;">Compruebe que el servidor DHCP se está ejecutando, que se ha creado un ámbito válido para los clientes WLAN y está activo, y que existe conectividad entre los puntos de acceso inalámbrico y el servidor DHCP. Dicho de forma más precisa, la conectividad es necesaria entre la LAN virtual (VLAN) de los puntos de acceso y el servidor DHCP para permitir que los clientes WLAN adquieran el arrendamiento de una IP).</td>
</tr>
</tbody>
</table>
  
###### Comprobar la configuración de los puntos de acceso inalámbrico
  
La tabla siguiente enumera una serie de comprobaciones que ha de realizar en los puntos de acceso inalámbrico para determinar si están funcionando adecuadamente.
  
**Tabla 8.14. Comprobaciones para el diagnóstico de los puntos de acceso inalámbrico**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Comprobación</th>
<th style="border:1px solid black;" >Detalle</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Compruebe la configuración IP de los puntos de acceso y la conectividad con IAS</td>
<td style="border:1px solid black;">Muchos puntos de acceso ofrecen una función para probar la conectividad básica (como el ping). Intente hacer ping a los servidores IAS principal y secundario (otra posibilidad es intentar hacer ping a los puntos de acceso de los servidores IAS principal y secundario).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Compruebe la configuración RADIUS de los puntos de acceso</td>
<td style="border:1px solid black;">Compruebe la dirección IP y los valores de los puertos configurados en el punto de acceso para los servidores RADIUS principal y secundario. Asegúrese de que coinciden con la configuración de los servidores IAS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Compruebe la entrada de cliente RADIUS en el servidor o servidores IAS.</td>
<td style="border:1px solid black;">Compruebe que los servidores IAS principal y secundario cuentan con una entrada de cliente RADIUS para este punto de acceso. Si IAS recibe una solicitud RADIUS desde un dispositivo no configurado como cliente, registrará un error en el registro del sistema.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Compruebe el secreto del cliente RADIUS</td>
<td style="border:1px solid black;">Puede que sea difícil comprobar visualmente el secreto del cliente RADIUS, puesto que, en algunas ocasiones, no se puede visualizar el secreto RADIUS una vez registrado en el punto de acceso. Si el valor configurado en la entrada de cliente RADIUS de IAS difiere del configurado en el punto de acceso, IAS registrará un error en el registro de sucesos del sistema.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Compruebe la revisión del firmware del punto de acceso</td>
<td style="border:1px solid black;">Compruebe que el firmware del punto de acceso está actualizado. Consulte las actualizaciones disponibles en el sitio Web del proveedor.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Compruebe el servidor DHCP</td>
<td style="border:1px solid black;">Compruebe que el servidor DHCP se está ejecutando, que se ha creado un ámbito válido para los clientes WLAN y que está activo, y que, asimismo, existe conectividad entre los puntos de acceso inalámbrico y el servidor DHCP. Dicho de forma más precisa, la conectividad es necesaria entre VLAN de los puntos de acceso y el servidor DHCP para permitir que los clientes WLAN adquieran el arrendamiento de una IP.</td>
</tr>
</tbody>
</table>
  
###### Comprobar conectividad WAN
  
El origen de los errores de WLAN puede radicar en problemas de conectividad WAN entre diversos componentes. La tabla siguiente enumera los elementos con más posibilidades de ser la causa de los problemas.
  
**Tabla 8.15. Comprobaciones para el diagnóstico de WAN**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Comprobación</th>
<th style="border:1px solid black;" >Detalle</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Autenticación de puntos de acceso inalámbrico a servidores IAS remotos</td>
<td style="border:1px solid black;">Pruebe la conectividad simple entre el punto de acceso y los servidores IAS principal y secundario. Para ello, la mayoría de los puntos de acceso disponen de un simple comando <strong>ping</strong> o <strong>traceroute</strong>.
Si existen servidores de seguridad o enrutadores filtrando el tráfico entre los sitios en cuestión, debe comprobar que se permite la autenticación RADIUS y el tráfico de información de cuenta (las solicitudes junto con las respuestas en los puertos de Protocolo de datagrama de usuarios (UDP), 1812 y 1813).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Controladores de dominio que replican mediante WAN</td>
<td style="border:1px solid black;">Los problemas de replicación entre controladores de dominio pueden aparecer incluso donde hay conectividad IP. Una latencia excesiva puede originar errores en las comunicaciones RPC entre los controladores de dominio. Para comprobarlo, utilice la herramienta dcdiag descrita en la sección &quot;Comprobar Active Directory y Servicios de red&quot; de este capítulo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Cliente WLAN y servidor DHCP</td>
<td style="border:1px solid black;">En los casos en que el servidor DHCP no se encuentre en la misma LAN que los puntos de acceso y que los clientes WLAN autenticados, deberá configurar un agente de retransmisión BOOTP/DHCP para reenviar las solicitudes al servidor DHCP correcto de la red remota.</td>
</tr>
</tbody>
</table>
  
#### Herramientas y técnicas para la solución de problemas
  
En esta sección se describen algunas de las técnicas y herramientas útiles para la solución de problemas.
  
##### Comprobación del estado de la carpeta de conexiones de red del cliente
  
La carpeta Conexiones de red y los iconos de notificación de la bandeja de sistema de Windows XP proporcionan información sobre el estado de la autenticación WLAN.
  
En la carpeta Conexiones de red (en el **Panel de control**), el texto de estado bajo el adaptador de red inalámbrico describe el estado actual de la conexión. Al resaltar el adaptador, se visualiza información adicional sobre la conexión en el panel **Detalles** de la carpeta Conexiones de red. Al deshabilitar y volver a habilitar el adaptador, se visualiza el estado del adaptador cuando se intenta conectar y autenticar a la WLAN. Esta información puede resultar muy útil cuando se depuran los problemas de conexión del cliente.
  
Haga clic con el botón secundario en el icono del adaptador y, a continuación, en **Estado** para comprobar la fuerza de la señal WLAN (en la ficha **General**) y los detalles de la dirección IP (en la ficha **Compatibilidad**).
  
##### Visualización de los sucesos de autenticación IAS en el registro de sucesos
  
Los sucesos fallidos o con éxito en la autenticación del cliente (que se graban en el registro de sucesos del sistema en los servidores IAS) pueden resultar útiles para la solución de problemas. El registro de sucesos se habilita de forma predeterminada tanto para las solicitudes de autenticación fallidas como para las satisfactorias. Este parámetro se puede modificar desde la ficha **Servicio** para las propiedades del servidor IAS en la MMC del **Servicio de autenticación de Internet**.
  
Consultar estos sucesos es útil para solucionar los problemas en la autenticación. En la siguiente tabla se enumeran los tipos de sucesos generados por IAS.
  
**Tabla 8.16. Sucesos de solicitud de autenticación IAS**

 
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Suceso IAS</th>
<th style="border:1px solid black;" >Importancia</th>
<th style="border:1px solid black;" >Categoría del suceso</th>
<th style="border:1px solid black;" >Origen del suceso</th>
<th style="border:1px solid black;" >Id. de suceso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Acceso concedido</td>
<td style="border:1px solid black;">Un usuario o equipo se autenticó satisfactoriamente y se le concedió acceso a WLAN.</td>
<td style="border:1px solid black;">Información</td>
<td style="border:1px solid black;">IAS</td>
<td style="border:1px solid black;">1</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Acceso denegado</td>
<td style="border:1px solid black;">Se denegó un intento de acceso (motivo expuesto en el texto del suceso).</td>
<td style="border:1px solid black;">Advertencia</td>
<td style="border:1px solid black;">IAS</td>
<td style="border:1px solid black;">2</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Descartado</td>
<td style="border:1px solid black;">El intento de acceso se descartó por agotar el tiempo de espera.</td>
<td style="border:1px solid black;">Error</td>
<td style="border:1px solid black;">IAS</td>
<td style="border:1px solid black;">3</td>
</tr>
</tbody>
</table>
  
Cada suceso contiene información detallada sobre la solicitud de autenticación. Esta información incluye:
  
-   Nombre de cliente
  
-   Dirección IP e identificador del punto de acceso
  
-   Tipo de cliente (debe ser "Inalámbrica-IEEE 802.11")
  
-   Nombre de la directiva de acceso remoto
  
-   Autenticación y tipo de EAP
  
-   Código y descripción del motivo
  
Si la autenticación da error, los códigos y descripciones del motivo suelen indicar el problema preciso (aunque a veces el motivo facilitado es ambiguo o engañoso). En la siguiente tabla se exponen los códigos de motivo disponibles.
  
**Tabla 8.17. Códigos de motivo de los sucesos de solicitud de autenticación IAS**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Código de motivo</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">00</td>
<td style="border:1px solid black;">Correcto</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">01</td>
<td style="border:1px solid black;">Error interno</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">02</td>
<td style="border:1px solid black;">Acceso denegado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">03</td>
<td style="border:1px solid black;">Solicitud mal formulada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">04</td>
<td style="border:1px solid black;">Catálogo global no disponible</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">05</td>
<td style="border:1px solid black;">Dominio no disponible</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">06</td>
<td style="border:1px solid black;">Servidor no disponible</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">07</td>
<td style="border:1px solid black;">No existe el dominio</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">08</td>
<td style="border:1px solid black;">No existe el usuario</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">16</td>
<td style="border:1px solid black;">Error en autenticación</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">17</td>
<td style="border:1px solid black;">Error al cambiar contraseña</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">18</td>
<td style="border:1px solid black;">Tipo de autenticación no compatible</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">32</td>
<td style="border:1px solid black;">Sólo usuarios locales</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">33</td>
<td style="border:1px solid black;">Debe cambiar la contraseña</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">34</td>
<td style="border:1px solid black;">Cuenta deshabilitada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">35</td>
<td style="border:1px solid black;">Cuenta caducada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">36</td>
<td style="border:1px solid black;">Cuenta bloqueada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">37</td>
<td style="border:1px solid black;">Horas de inicio de sesión no válidas</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">38</td>
<td style="border:1px solid black;">Restricción de cuenta</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">48</td>
<td style="border:1px solid black;">No coincide ninguna directiva</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">64</td>
<td style="border:1px solid black;">Marcado bloqueado</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">65</td>
<td style="border:1px solid black;">Marcado deshabilitado</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">66</td>
<td style="border:1px solid black;">Tipo de autenticación no válido</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">67</td>
<td style="border:1px solid black;">Estación de llamada no válida</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">68</td>
<td style="border:1px solid black;">Horas de marcado no válidas</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">69</td>
<td style="border:1px solid black;">Estación llamada no válida</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">70</td>
<td style="border:1px solid black;">Tipo de puerto no válido</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">71</td>
<td style="border:1px solid black;">Restricción no válida</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">80</td>
<td style="border:1px solid black;">No hay registros</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">96</td>
<td style="border:1px solid black;">Tiempo de espera de sesión agotado</td>
</tr>
</tbody>
</table>
  
En algunos casos, la información extraída de las entradas del registro de sucesos no es suficiente para diagnosticar la causa del problema. En estos casos, puede que necesite habilitar el seguimiento en el cliente y en el servidor IAS. En los procedimientos siguientes se describe el modo de hacerlo.
  
##### Habilitación y deshabilitación del seguimiento en equipos cliente
  
Windows admite un seguimiento detallado de la información en la mayoría de los componentes para facilitar el diagnóstico de los problemas que puedan surgir. La habilitación del seguimiento para un componente hace que se escriban los resultados del diagnóstico en los archivos de registro de texto, al tiempo que proporciona más detalles que los registros de sucesos.
  
Para obtener información pormenorizada sobre el proceso de autenticación WLAN, debe habilitar el seguimiento de EAP a través de los componentes de LAN (EAPOL) y del Servicio de acceso remoto - Seguridad de la capa de transporte (RASTLS) utilizando el comando **netsh**. Una vez habilitado el seguimiento, intente de nuevo el proceso de autenticación y examine los archivos Eapol.log y Rastls.log en busca de algún tipo de indicaciones sobre los problemas (estos archivos se grabarán en la carpeta %Systemroot%\\Tracing).
  
**Para habilitar el seguimiento en equipos cliente**
  
-   Ejecute los siguientes comandos:
  
    **netsh ras set tracing eapol enabled**
  
    **netsh ras set tracing rastls enabled**
  
**Para deshabilitar el seguimiento en equipos cliente**
  
-   Ejecute los siguientes comandos:
  
    **netsh ras set tracing eapol disabled**
  
    **netsh ras set tracing rastls disabled**
  
    **Nota:** el seguimiento consume una gran cantidad de recursos del sistema y crea archivos de registro que crecen con celeridad. No olvide volver a deshabilitar el seguimiento cuando finalice la tarea de solución de problemas.
  
##### Habilitación y deshabilitación del seguimiento en el servidor IAS
  
La habilitación del seguimiento en IAS funciona de la misma forma que en el equipo cliente.
  
Puede utilizar el comando **netsh** para habilitar y deshabilitar el seguimiento en una gran variedad de componentes diversos relacionados con la autenticación de red. Los componentes cuya habilitación resulta más útil para el seguimiento de los problemas de autenticación 802.1X basada en PEAP son los siguientes:
  
-   **IASSAM (el archivo Iassam.log de la carpeta %Systemroot%\\tracing):** éste es el archivo de seguimiento más utilizado para los problemas de IAS, puesto que describe las funciones relacionadas con el descifrado (traducción entre distintos formatos) de nombres de usuario, el enlace a un controlador de dominio y la comprobación de credenciales. Se trata del "centro" de los archivos de seguimiento de IAS y suele ser necesario para depurar los problemas relacionados con la autenticación.
  
-   **RASTLS (el archivo Rastls.log de la carpeta %Systemroot%\\tracing):** este archivo de seguimiento se utiliza para todas las autenticaciones relacionadas con EAP y PEAP. Este registro contiene la mayor parte de la información vital para la depuración. No obstante, su lectura y comprensión es bastante compleja, de ahí que Microsoft tenga como objetivo publicar documentación que facilite la interpretación de esta información.
  
-   **RASCHAP (el archivo Raschap.log de la carpeta %Systemroot%\\tracing):** este archivo de seguimiento se utiliza para todas las operaciones de autenticación de contraseñas basadas en MS-CHAP v2 y otros CHAP.
  
La habilitación del seguimiento de los componentes IAS que se indican a continuación no suele ser necesaria para solucionar problemas de autenticación 802.1X, pero puede resultar útil para solucionar problemas de otra índole:
  
-   **IASRAD (el archivo Iasrad.log de la carpeta %Systemroot%\\tracing):** éste registra todas las operaciones relacionadas con el protocolo RADIUS. Asimismo, describe los puertos en los que el servidor escucha, etc. Puede resultar útil para depurar problemas de compatibilidad de los puntos de acceso inalámbrico.
  
-   **IASSDO (el archivo Iassdo.log de la carpeta %Systemroot%\\tracing):** el registro IASSDO contempla transacciones realizadas desde la interfaz de usuario a archivos MDB que almacenan el diccionario y la configuración del servidor. Se trata del registro utilizado para solucionar los problemas de cualquier servicio o los relacionados con la interfaz de usuario.
  
**Para habilitar el seguimiento en el servidor IAS**
  
1.  Ejecute el comando **netsh** correspondiente al tipo de información de seguimiento que necesite. Cuando solucione problemas relacionados con la autenticación 802.1X, los registros IASSAM, RASTLS y RASCHAP serán los que contengan la información más útil.
  
    **netsh ras set tracing iassam enabled**
  
    **netsh ras set tracing rastls enabled**
  
    **netsh ras set tracing raschap enabled**
  
    **netsh ras set tracing iasrad enabled**
  
    **netsh ras set tracing iassdo enabled**
  
    Otra posibilidad para habilitar el seguimiento de todas las categorías de componentes de red sería la ejecución del siguiente comando:
  
    **netshras set tracing \* enabled**
  
**Para deshabilitar el seguimiento en el servidor IAS**
  
1.  Ejecute uno o varios de los siguientes comandos **netsh** para deshabilitar el seguimiento de las categorías habilitadas en el procedimiento anterior:
  
    **netsh ras set tracing iassam disabled**
  
    **netsh ras set tracing rastls disabled**
  
    **netsh ras set tracing raschap disabled**
  
    **netsh ras set tracing iasrad disabled**
  
    **netsh ras set tracing iassdo disabled**
  
    Otra posibilidad para deshabilitar el seguimiento de todas las categorías de componentes de red sería la ejecución del siguiente comando:
  
    **netshras set tracing \* disabled**
  
    **Nota:** dado que el seguimiento consume recursos significativos del sistema, debe utilizarlo con moderación para identificar los problemas de la red. Una vez realizado el seguimiento o identificado el problema, deberá deshabilitar el seguimiento inmediatamente.
  
De forma predeterminada, los archivos de seguimiento IASSAM y RASTLS están establecidos en sólo 1 MB. Esto puede originar que se sobrescriba información valiosa en los archivos de registro durante grandes cargas. El procedimiento que sigue establece los registros de seguimiento en 10 MB. Cuando un archivo de registro alcanza el límite de 10 MB, se le cambia el nombre (a IASSAM.old y RASTLS.old) y se crea un nuevo archivo de registro. Esto mantiene un máximo de 20 MB de información en el servidor para cada tipo de seguimiento. Puede repetir este procedimiento para cualquier tipo de seguimiento con sólo sustituir el nombre de la categoría del seguimiento (como RASTLS y RASCHAP) por el nombre clave "IASSAM" utilizado en el procedimiento.
  
**Para establecer el archivo de registro de seguimiento IASSAM en 10 MB**
  
1.  Inicie Regedit.exe.
  
2.  Desplácese hasta la siguiente clave de Registro:
  
    **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Tracing**
  
3.  Busque la subclave **IASSAM**. Ésta debería tener un valor de Registro **MaxFileSize** (un tipo de **REG\_DWORD**). Edite este valor y establezca el valor de los datos como **0xA00000** (ésta es la representación hexadecimal de 10MB: el valor predeterminado sería 0x100000). Si lo desea, puede establecer un valor distinto a 10 MB, si bien los registros comenzarían a ser difíciles de administrar con un tamaño mayor.
  
    **Advertencia:** la edición incorrecta del Registro puede dañar el sistema gravemente. Antes de realizar cambios en el Registro, haga copias de seguridad de todos los datos importantes del equipo.
  
##### Habilitación del registro SChannel en el servidor IAS
  
SChannel es un proveedor de compatibilidad de seguridad (SSP) que admite varios protocolos de seguridad de Internet, como capa de sockets seguros (SSL) y seguridad de la capa de transporte (TLS). Si sospecha que existen problemas relacionados con el certificado de servidor IAS o si el registro RASTLS indica que existe algún problema con la creación de la sesión TLS, debe habilitar el registro SChannel tanto en el cliente como en el servidor. Los sucesos se registran en el registro de seguridad.
  
Siga el mismo procedimiento tanto en el equipo cliente, como en el servidor.
  
**Para habilitar el registro SChannel**
  
1.  Inicie Regedit.exe.
  
2.  Desplácese hasta la siguiente clave de Registro:
  
    **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\SecurityProviders\\SCHANNEL\\**
  
3.  Habilite sucesos SChannel detallados mediante la modificación del valor **EventLogging** de **1** (tipo **REG\_DWORD**, datos **0x00000001**) a **3** (tipo **REG\_DWORD**, datos **0x00000003**).
  
    **Advertencia:** la edición incorrecta del Registro puede dañar el sistema gravemente. Antes de realizar cambios en el Registro, debe hacer copias de seguridad de todos los datos importantes del equipo.
  
Cuando termine de solucionar problemas, asegúrese de deshabilitar el registro Schannel, puesto que consume recursos significativos del sistema e inundará el registro de sucesos con entradas no deseadas.
  
##### Herramientas de diagnóstico para el equipo Pocket PC
  
Windows XP cuenta con varias herramientas de diagnóstico de red. Los equipos Pocket PC, en cambio, disponen de relativamente pocas herramientas integradas en el sistema base. El proveedor del equipo Pocket PC, Microsoft y otras compañías proporcionan diversos tipos de herramientas para facilitar el diagnóstico de los problemas con estos equipos. Algunos ejemplos incluyen:
  
-   **Configuración IP y herramientas de diagnóstico:** herramientas tales como VXUtil o VXIPConfig de Cambridge Software.
  
-   Herramientas de diagnóstico de WLAN facilitadas por el proveedor del equipo Pocket PC.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo se han tratado los siguientes elementos necesarios para mantener el estado de la infraestructura de seguridad de WLAN:
  
-   Identificación de las tareas de mantenimiento esenciales.
  
-   Descripción de las tareas operativas, de supervisión, soporte técnico, modificación y optimización relacionadas con este entorno.
  
-   Descripción de los procedimientos y técnicas clave para la solución de problemas.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Referencias
  
Esta sección contiene vínculos a otras fuentes de información que sirven como referencia para las instrucciones proporcionadas en este capítulo:
  
-   Para obtener más información sobre la realización de copias de seguridad y la restauración de los servidores Windows, consulte la página "Backing up and restoring data" de Windows Server 2003 en Microsoft.com en:
  
    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/entserver/ctasks001.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/entserver/ctasks001.mspx)
  
-   Para obtener más información sobre la supervisión y administración, consulte la página "Microsoft Solutions for Management" en Microsoft.com en:
  
    [http://www.microsoft.com/technet/itsolutions/techguide/  
    msm/default.mspx](http://technet.microsoft.com/en-us/solutionaccelerators/default.aspx)
  
-   Para obtener más información sobre la optimización de IAS, consulte la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/deployguide/dnsbk\_ias\_rziy.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/deployguide/dnsbk_ias_rziy.mspx)
  
-   Para obtener más información sobre la solución de problemas de componentes de red inalámbricos, consulte las siguientes direcciones URL:
  
    <http://support.microsoft.com/default.aspx?scid=313242>
  
    [http://www.microsoft.com/technet/prodtechnol/winxppro/  
    maintain/wifitrbl.mspx](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/wifitrbl.mspx)
  
-   Para obtener más información sobre la solución de problemas de IAS, consulte la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/entserver/sag\_ias\_tshoot\_node.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/entserver/sag_ias_tshoot_node.mspx)
  
-   Para obtener más información sobre la configuración IP y las herramientas de diagnóstico tales como VXUtil o VXIPConfig, consulte la siguiente dirección URL:
  
    <http://www.cam.com/windowsce.html>
  
(Este artículo contiene referencias a guías de otros productos y vínculos a sitios Web que sólo están disponibles en inglés.)
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Apéndice A: Uso de PEAP en la empresa
  
Microsoft® ha producido dos soluciones para la seguridad en redes de área local inalámbrica (WLAN). La primera solución *Solución de Seguridad de LAN inalámbricas — Servicios de Certificate Server de Microsoft Windows Server 2003* utiliza certificados de cliente para autenticar clientes inalámbricos y está pensada principalmente para organizaciones empresariales grandes. La segunda, *Seguridad en LAN inalámbricas con PEAP y contraseñas* (el tema de esta guía), utiliza contraseñas y el protocolo de autenticación extensible protegido (PEAP) para autenticar clientes inalámbricos. Esta última se ha escrito fundamentalmente para organizaciones pequeñas y medianas. No obstante, no hay nada sobre PEAP que restrinja su uso a organizaciones más pequeñas. Las organizaciones empresariales grandes también pueden recurrir a PEAP y a la autenticación por contraseña para asegurar sus WLAN.
  
Si forma parte de una organización grande que está planeando implementar PEAP con contraseñas, este apéndice le mostrará cómo utilizar las secciones de ambas soluciones para poder implementarlo. Ambas soluciones cuentan con la misma arquitectura técnica y componentes idénticos, así que es relativamente sencillo tomar el contenido centrado en la empresa de la primera solución y reemplazar los protocolos de autenticación de certificados por los protocolos de PEAP y contraseñas. El objetivo es facilitar una guía combinada que incluya detalles relevantes para una solución WLAN para empresas, como una delegación administrativa avanzada, registro de RADIUS y la separación de funciones del servidor, pero con contraseñas para autenticar clientes inalámbricos.
  
A lo largo de este apéndice, por razones de brevedad, el término "solución EAP-TLS" se utilizará para hacer alusión a la primera solución (*Solución de Seguridad de LAN inalámbricas — Servicios de Certificate Server de Microsoft Windows Server 2003*), mientras que el término "solución PEAP" hará referencia a la segunda (*Seguridad en LAN inalámbricas con PEAP y contraseñas*). Protocolo de autenticación extensible-Seguridad de la capa de transporte es el nombre de certificado de cliente basado en el protocolo de autenticación utilizado en la primera solución.
  
### Aspectos necesarios de la solución EAP-TLS
  
Desde que se confeccionara la guía de la solución EAP-TLS para organizaciones grandes, ésta se ha convertido en la referencia principal. Incluye el planeamiento, la implementación y los detalles operativos (como la delegación de la administración) que probablemente sean de mayor interés para organizaciones grandes. Después de la tabla, encontrará una lista de los capítulos de la solución EAP-TLS. Para cada capítulo se proporciona una descripción que detalla si el contenido de esta solución es relevante o no para la guía "combinada". Asimismo, se destacan aquellos casos en los que el contenido de la solución PEAP se debe utilizar en lugar de las instrucciones de la solución EAP-TLS.
  
A modo de referencia, la siguiente tabla contempla la asignación entre los capítulos de ambas soluciones. Debido a diferencias de alcance y utilización de la tecnología, la asignación entre los capítulos no es uno a uno.
  
**Tabla A.1. Asignación de los capítulos entre las soluciones EAP-TLS y PEAP**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Solución EAP-TLS</th>
<th style="border:1px solid black;" >Solución PEAP</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Capítulo 1: Información general</td>
<td style="border:1px solid black;">Capítulo 1: Seguridad en LAN inalámbricas con PEAP y contraseñas</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Capítulo 2: Determinación de una estrategia para redes inalámbricas seguras</td>
<td style="border:1px solid black;">Introducción: Elección de una estrategia para la seguridad en LAN inalámbricas</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Capítulo 3: Arquitectura de la solución para una LAN inalámbrica segura</td>
<td style="border:1px solid black;">Capítulo 2: Planeamiento de la implementación de seguridad en LAN inalámbricas</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Capítulo 4: Designing the Public Key Infrastructure</td>
<td style="border:1px solid black;">Capítulo 2: Planeamiento de la implementación de seguridad en LAN inalámbricas</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Capítulo 5: Diseño de una infraestructura de RADIUS para la seguridad de LAN inalámbricas</td>
<td style="border:1px solid black;">Capítulo 2: Planeamiento de la implementación de seguridad en LAN inalámbricas</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Capítulo 6: Diseño de la seguridad para LAN inalámbrica mediante 802.1X</td>
<td style="border:1px solid black;">Capítulo 2: Planeamiento de la implementación de seguridad en LAN inalámbricas</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"> </td>
<td style="border:1px solid black;">Capítulo 3: Preparación del entorno</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Capítulo 7: Implementing the Public Key Infrastructure</td>
<td style="border:1px solid black;">Capítulo 4: Creación de la entidad emisora de certificados de red</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Capítulo 8: Implementación de la infraestructura de RADIUS para la seguridad de LAN inalámbricas</td>
<td style="border:1px solid black;">Capítulo 5: Creación de la infraestructura de seguridad de LAN inalámbricas</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Capítulo 9: Implementing Wireless Security Using 802.1X</td>
<td style="border:1px solid black;">Capítulo 6: Configuración de clientes de LAN inalámbricas</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Capítulo 10: Introducción a la guía de operaciones</td>
<td style="border:1px solid black;">Capítulo 8: Mantenimiento de soluciones de seguridad en LAN inalámbricas</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Capítulo 11: Administración de la infraestructura de claves públicas</td>
<td style="border:1px solid black;">Capítulo 8: Mantenimiento de soluciones de seguridad en LAN inalámbricas</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Capítulo 12: Administración de la infraestructura de seguridad de RADIUS y LAN inalámbrica</td>
<td style="border:1px solid black;">Capítulo 8: Mantenimiento de soluciones de seguridad en LAN inalámbricas</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Capítulo 13: Guía de prueba</td>
<td style="border:1px solid black;">Capítulo 7: Prueba de soluciones de seguridad en LAN inalámbricas</td>
</tr>
</tbody>
</table>
  
Cabe destacar que la solución EAP-TLS se estructuró intencionadamente para mantener la infraestructura de claves públicas, RADIUS y los componentes WLAN lo más independientes entre sí posible. Con ello se perseguía permitir volver a utilizar estos componentes en otras aplicaciones. Esto explica que existan algunas repeticiones en la solución EAP-TLS. Por ejemplo, los capítulos sobre la infraestructura de claves públicas y RADIUS incluyen instrucciones sobre la creación de servidores puesto que, en organizaciones grandes, es posible que la instalación de los servidores IAS y de las entidades emisoras de certificados sea responsabilidad de distintos grupos dentro de TI. Además, algunos de los pasos lógicos descritos en los capítulos de diseño e implementación pueden resultar engañosos en el contexto de una solución PEAP. Por tanto, debe leer la solución PEAP para obtener una introducción general sobre el proceso completo y, a continuación, volver a la solución EAP-TLS para conocer detalles específicos sobre el diseño e implementación.
  
Las siguientes secciones contienen las descripciones sobre cómo utilizar los capítulos de la solución EAP-TLS en relación con los capítulos de la solución PEAP.
  
#### Capítulo 1: Información general
  
El capítulo 1 consiste en una introducción general de la solución y contiene breves resúmenes de cada capítulo y apéndice de la guía. Como trabajará principalmente con la guía de EAP-TLS, debe utilizar el capítulo 1 de esta solución.
  
#### Capítulo 2: Determinación de una estrategia para redes inalámbricas seguras
  
El contenido de este capítulo es muy parecido al contenido de la introducción, "Elección de una estrategia para la seguridad en LAN inalámbricas", de la solución PEAP. La introducción a la solución PEAP hace las veces de un prefacio de ambas soluciones, así que debe utilizar éste en lugar de recurrir al capítulo 2 de la solución EAP-TLS.
  
#### Capítulo 3: Arquitectura de la solución para una LAN inalámbrica segura
  
Este capítulo proporciona una introducción general sobre la arquitectura de la solución WLAN basada en certificados. Es relevante para todos los siguientes elementos, excepto para el primero:
  
-   Descripción del funcionamiento de 802.1X con EAP-TLS (certificados). En su lugar, debe consultar la descripción contemplada en el capítulo 2, "Planeamiento de la implementación de seguridad en LAN inalámbricas" de la solución PEAP.
  
-   Descripción de la organización de destino.
  
-   Lista de los criterios clave de diseño de la solución.
  
-   Ilustración de la utilización de diversos componentes del servidor en distintas ubicaciones de la organización.
  
-   Descripción de cómo se puede escalar la solución.
  
-   Ejemplos de utilización de elementos de la solución para admitir otras aplicaciones de red como la seguridad 802.1X con cable y la red privada virtual (VPN).
  
Las referencias incluidas a la entidad emisora de certificados también pueden ser útiles en el capítulo siguiente.
  
#### Capítulo 4: Designing the Public Key Infrastructure
  
Este capítulo contiene una descripción detallada del proceso de planeamiento de una infraestructura de claves públicas sencilla. La solución PEAP también contiene instrucciones para una entidad emisora de certificados sencilla con un solo propósito. Aunque no necesite emitir certificados a los clientes WLAN, debe considerar la utilización del siguiente capítulo como ayuda en el diseño de la infraestructura de claves públicas. Cuanto más grande sea la organización, más probable es que necesite certificados en lugar de simples autenticaciones de red. Este capítulo le ayudará a diseñar una infraestructura de claves públicas más flexible y sólida que la que presenta la solución PEAP.
  
#### Capítulo 5: Diseño de una infraestructura de RADIUS para la seguridad de LAN inalámbricas
  
Debe seguir las instrucciones proporcionadas en este capítulo de la solución EAP-TLS.
  
#### Capítulo 6: Diseño de la seguridad para LAN inalámbrica mediante 802.1X
  
Debe seguir las instrucciones proporcionadas en este capítulo de la solución EAP-TLS.
  
#### Capítulo 7: Implementing the Public Key Infrastructure
  
Este capítulo sólo es relevante si ha decidido implementar una infraestructura de claves públicas completa tal y como se mencionó anteriormente. De lo contrario, siga el capítulo 4 de la solución PEAP, "Creación de la entidad emisora de certificados de red".
  
#### Capítulo 8: Implementación de la infraestructura de RADIUS para la seguridad de LAN inalámbricas
  
Debe seguir las instrucciones proporcionadas en este capítulo. Para obtener información complementaria, lea el capítulo 5 de la solución PEAP, "Creación de la infraestructura de seguridad de LAN inalámbricas".
  
#### Capítulo 9: Implementing Wireless Security Using 802.1X
  
Debe seguir las instrucciones dadas en el capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas" y en el capítulo 6, "Configuración de clientes de LAN inalámbricas", de la solución PEAP sobre cómo configurar la directiva de acceso remoto IAS y la configuración del objeto de directiva de grupo del cliente. El capitulo 5 de la solución PEAP también ofrece útiles detalles que no se tratan en la solución EAP-TLS sobre la configuración de puntos de acceso inalámbrico y secuencias de comandos para automatizar la entrada de clientes RADIUS y la replicación de la configuración de IAS.
  
#### Capítulos 10, 11 y 12 sobre el funcionamiento de la solución
  
Debe seguir las instrucciones proporcionadas en estos capítulos de la solución EAP-TLS. Además, debe leer las instrucciones sobre la solución de problemas con WLAN proporcionadas en el capítulo 8 de la solución PEAP, "Mantenimiento de soluciones de seguridad en LAN inalámbricas". Los procedimientos y técnicas detallados en este capítulo suponen un complemento útil a los procedimientos de los capítulos de la solución EAP-TLS.
  
#### Capítulo 13: Guía de prueba
  
Debe utilizar el contenido de este capítulo. Asimismo, si ha optado por no implementar una infraestructura de claves públicas completa como se describe en el capítulo 4 de la solución EAP-TLS, "Designing Key Infraestructure", haga caso omiso de las pruebas de este capítulo relacionadas con dicha infraestructura.
  
#### Secuencias de comandos
  
Las secuencias de comandos utilizadas en la solución PEAP se desarrollaron a partir de las secuencias de comandos de la solución EAP-TLS. No obstante, aunque las secuencias de comandos de PEAP contienen una mayor funcionalidad que las de EAP-TLS, no constituyen un superconjunto exacto. Por ejemplo, las secuencias de comandos de EAP-TLS contienen funciones de supervisión de la entidad emisora de certificados más sofisticadas. En la mayoría de los casos se deben utilizar las secuencias de comandos facilitadas en la solución PEAP. Sin embargo, es posible que desee instalar las secuencias de comandos de ambas soluciones en carpetas separadas y utilizar cada una de ellas según sea apropiado. Las secuencias de comandos se proporcionan como ejemplos básicos para ilustrar técnicas. Por lo tanto, no dude en modificarlos para adaptarlos mejor a sus necesidades.
  
(Este artículo contiene referencias a guías de otros productos y vínculos a sitios Web que sólo están disponibles en inglés.)
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Apéndice B: Uso de WPA en la solución
  
La solución de red de área local inalámbrica (WLAN) descrita en esta documentación funciona correctamente tanto con la protección mediante WEP (privacidad equivalente por cable) dinámica como con la protección mediante WPA (acceso inalámbrico protegido) para WLAN. Las diferencias de implementación entre ambas son mínimas y se documentan en este apéndice.
  
En la actualidad existen ciertas dificultades al usar WPA, entre las que se encuentran:
  
-   **Configuración manual de WPA:** la configuración de WPA en clientes Windows® XP mediante directivas de grupo no es compatible con las versiones de Windows® anteriores a Windows Server™ 2003 Service Pack 1. Hasta que no disponga de Service Pack 1 y lo instale en la empresa, deberá configurar los equipos cliente manualmente (no se pueden ejecutar secuencias de comandos de la configuración de WLAN para Windows XP). No es necesario instalar Service Pack 1 en equipos cliente, controladores de dominio o servidores IAS, sino sólo en el servidor en el que modifica el objeto de directiva de grupo de la configuración de WLAN.
  
-   **Disponibilidad restringida para clientes WLAN:** en el momento de redacción de este documento, Microsoft® sólo ofrece compatibilidad de WPA con Windows XP Service Pack 1 y posteriores.
  
-   **Disponibilidad para hardware compatible con WPA:** aunque ahora ya es obligatorio que todo hardware con certificado Wi-fi sea compatible con WPA, puede que el equipo de red existente deba actualizarse para ser compatible con WPA. Deberá obtener actualizaciones de firmware para todos los puntos de acceso o adaptadores de red que actualmente no sean compatibles con WPA. En algunos casos (poco frecuentes), puede que deba reemplazar el equipo si el fabricante no proporciona actualizaciones de WPA.
  
#### En esta página
  
[](#eeaa)[Uso de WPA en lugar de WEP](#eeaa)  
[](#edaa)[Migración de WEP a WPA](#edaa)  
[](#ecaa)[Referencias](#ecaa)
  
### Uso de WPA en lugar de WEP
  
Aunque gran parte de la guía se aplica tanto a WPA como a la WEP dinámica, existen dos puntos principales en la documentación en los que se ofrecen distintas instrucciones:
  
-   La sección "Creación de una directiva de acceso remoto IAS para WLAN" del capítulo 5 ("Creación de la infraestructura de seguridad de LAN inalámbricas").
  
-   La sección "Creación de objetos de directiva de grupo de la configuración de WLAN" del capítulo 6 ("Configuración de clientes de LAN inalámbricas").
  
#### Creación de una directiva de acceso remoto de IAS para WLAN con WPA
  
Para utilizar la protección de WLAN con WPA en lugar de con WEP dinámica, debe establecer el valor de tiempo de espera de la sesión en ocho horas (y no en 60 minutos). WPA dispone de un mecanismo integrado que genera claves de cifrado de WLAN, de forma que no necesita forzar a los clientes a volver a autenticarse con frecuencia. Un valor de ocho horas es suficiente para asegurar que los clientes dispongan de credenciales actualizadas válidas (por ejemplo, garantiza que un cliente no permanezca conectado durante un tiempo excesivo una vez que la cuenta se ha deshabilitado). En entornos de alta seguridad, puede reducir este valor de tiempo de espera, si es necesario.
  
Utilice el siguiente procedimiento, que se detalla en la sección "Modificación de la configuración del perfil de la directiva de acceso a WLAN" del capítulo 5, "Creación de la infraestructura de seguridad de LAN inalámbricas", para configurar el perfil de la directiva de acceso remoto:
  
**Para modificar la configuración del perfil de la directiva de acceso inalámbrico:**
  
1.  En el complemento MMC del Servicio de autenticación de Internet, abra las propiedades de la directiva **Permitir acceso a LAN inalámbrica** y haga clic en **Modificar perfil**.
  
2.  En la ficha **Restricciones de marcado** del campo **Minutos que el cliente puede estar conectado (tiempo de espera de sesión)**, escriba *480* (480 minutos u 8 **horas).
  
3.  En la ficha **Avanzadas**, agregue el atributo **Ignorar propiedades de acceso telefónico del usuario** y establézcalo en **True**; a continuación, agregue el atributo **Acción-Terminación** y establézcalo en **RADIUS Request**.
  
También debe modificar el tiempo de espera de la sesión en el punto de acceso inalámbrico para que se halle en el mismo nivel del valor de tiempo de espera establecido en este procedimiento (o lo supere).
  
#### Configuración manual de WLAN en Windows XP para WPA
  
Hasta que no disponga de compatibilidad con el objeto de directiva de grupo en Windows Server 2003 Service Pack 1, deberá configurar WPA en el equipo cliente de forma manual. WPA es compatible con Windows XP Service Pack 1 con la descarga del cliente WPA instalada (o en Windows XP Service Pack 2).
  
**Nota:** cuando disponga de compatibilidad con el objeto de directiva de grupo, podrá utilizar el siguiente procedimiento para crear una directiva de red inalámbrica con la misma configuración.
  
**Para configurar manualmente la WLAN con WPA:**
  
1.  Abra las propiedades de la interfaz **Red inalámbrica**. Si en la lista **Redes disponibles** aparece WLAN, selecciónela y haga clic en **Configurar** o en **Agregar** (en la sección **Redes preferidas**).
  
2.  Escriba el nombre de la WLAN en el campo **Nombre de red (SSID)** (si no aparece ya) y, en el campo **Descripción**, escriba una descripción para la red.
  
    **Nota:** si ya posee una WLAN configurada y desea ejecutarla en paralelo con la WLAN basada en 802.1X de esta solución, debe utilizar un Identificador del conjunto de servicios (SSID) para la nueva WLAN. Este nuevo SSID deberá utilizarse aquí.
  
3.  En la sección **Clave de red inalámbrica**, seleccione **WPA** (no seleccione **WPA PSK**) como el tipo de **Autenticación de red** y **TKIP** como el tipo de **Cifrado de datos**. Si el hardware es compatible, seleccione el estándar de cifrado avanzado más seguro (**AES** en lugar de **TKIP**).
  
4.  Haga clic en la ficha **IEEE 802.1x** y seleccione **EAP protegido (PEAP)** de la lista desplegable **Tipo de EAP**.
  
5.  Haga clic en el botón **Configuración** para modificar la configuración PEAP. En la lista **Entidad emisora raíz de confianza**, seleccione el certificado de entidad emisora raíz para la entidad emisora, que es la que instaló para emitir certificados del servidor IAS (consulte el capítulo 4 para obtener más información).
  
    **Importante:** si necesita instalar de nuevo la entidad emisora desde cero (no sólo restaurarla desde la copia de seguridad), deberá modificar la configuración del cliente y seleccionar el certificado de entidad emisora para la nueva entidad emisora.
  
6.  Asegúrese de que selecciona **Contraseña protegida (EAP-MS-CHAP v2)** en **Seleccione el método de autenticación** y compruebe la opción **Habilitar reconexión rápida**.
  
7.  Cierre cada una de las ventanas de propiedades haciendo clic en **Aceptar**.
  
#### Configuración de Pocket PC 2003 para WPA
  
Cuando se redactó este documento, WPA no era compatible en su origen con Pocket PC 2003. Sin embargo, puede que se implemente en el futuro. Es posible que otros fabricantes también ofrezcan compatibilidad con WPA para Pocket PC.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Migración de WEP a WPA
  
Si ha implementado una solución WLAN segura basada en WEP dinámica y desea migrar a WPA, deberá seguir los pasos que se indican en esta sección. Antes de realizar la migración, debe asegurarse de que ha implementado los elementos de compatibilidad con WPA, tanto el software (por ejemplo, el componente WPA de Windows XP) como el hardware (actualizaciones del firmware del punto de acceso y del controlador del adaptador de red). Toda referencia en este procedimiento sobre la configuración de WPA en objetos de directiva de grupo es válida solamente si estos objetos se modifican desde Windows Server 2003 Service Pack 1 o posterior. En el momento de redacción del documento, este Service Pack aún no se ha lanzado al mercado. Si no utiliza Windows Server 2003 Service Pack 1 o una versión posterior, siga las instrucciones de la sección "Configuración manual de WLAN en Windows XP para WPA" de este apéndice.
  
**Para realizar una migración de WEP a WPA cuando el punto de acceso admite simultáneamente WEP dinámica y WPA:**
  
1.  Configure todos los puntos de acceso inalámbrico para que admitan WEP dinámica y WPA a la vez.
  
2.  Cree un nuevo objeto de directiva de grupo de la configuración del cliente WLAN. Cree una directiva de red inalámbrica que establezca la configuración adecuada para WPA (consulte el procedimiento de la sección "Configuración manual de WLAN en Windows XP para WPA" de este apéndice). A continuación, deshabilite el objeto de directiva de grupo de la WEP actual y habilite el de WPA para que todas las configuraciones de WPA se envíen a todos los clientes. Los clientes comenzarán a utilizar WPA en la WLAN una vez se haya actualizado el objeto de directiva de grupo.
  
    **Nota:** si configura los clientes de forma manual, deberá deshabilitar el objeto de directiva de grupo que contenga la configuración WEP, ya que, de no hacerlo, el objeto de directiva de grupo sobrescribirá la configuración WPA manual.
  
3.  Finalmente, debe actualizar el tiempo de espera de la sesión de la directiva de acceso remoto IAS y de la sesión de cliente en el punto de acceso (tal y como se describe en la sección sobre la directiva de acceso remoto IAS anterior de este apéndice).
  
**Para realizar una migración de WEP a WPA cuando el punto de acceso no admite WEP y WPA simultáneamente:**
  
1.  Cree un nuevo SSID de WLAN para la red WPA.
  
2.  Modifique el objeto de directiva de grupo de la configuración de red del cliente y agregue el nuevo SSID con los parámetros de WPA (tal y como se describe en la sección "Configuración manual de WLAN en Windows XP para WPA" anterior de este apéndice). Si configura los clientes de forma manual, deberá hacerlo con el nuevo SSID y, asimismo, con la configuración de WPA para ese SSID. En cualquier caso, no quite la configuración del SSID de la WEP anterior.
  
3.  De forma simultánea, vuelva a configurar los puntos de acceso que admitían WEP para que sean compatibles con WPA y modifique el SSID del punto de acceso. A medida que vaya configurando cada punto de acceso, los clientes cambiarán al nuevo SSID y utilizarán WPA.
  
4.  Una vez que haya reconfigurado todos los puntos de acceso, podrá actualizar las directivas de acceso remoto en todos los servidores IAS. Será necesario aumentar el valor de tiempo de espera de la sesión en la directiva de acceso remoto (de 60 minutos a 8 horas) y, además, modificar la misma configuración en los puntos de acceso inalámbrico (tal y como se describe en la sección sobre la directiva de acceso remoto IAS anterior de este apéndice).
  
5.  Una vez que ha finalizado la migración, puede quitar el SSID de la WEP del objeto de directiva de grupo.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Referencias
  
Esta sección incluye referencias a otra información complementaria importante u otro material informativo de relevancia para este apéndice.
  
-   Artículo "Wi-Fi Protected Access™ (WPA) Overview" de marzo de 2003 de "The Cable Guy" en la siguiente dirección URL:
  
    [http://www.microsoft.com/technet/columns/  
    cableguy/cg0303.mspx](http://technet.microsoft.com/es-es/library/bb877996.aspx)
  
-   Artículo 815485 de Microsoft Knowledge Base, "Introducción a la actualización de seguridad de WPA inalámbrico en Windows XP", disponible en la siguiente dirección URL:
  
    <http://support.microsoft.com/default.aspx?scid=kb;es;815485>
  
-   Anuncio de prensa de Microsoft sobre la disponibilidad de WPA, que puede consultar en la siguiente dirección URL:
  
    [http://www.microsoft.com/presspass/press/2003/mar03/03-31WiFiProtectedAccessPR.asp](http://www.microsoft.com/presspass/press/2003/mar03/03-31wifiprotectedaccesspr.asp)
  
-   Notas del producto "Wireless 802.11 Security with Windows XP", disponible en la siguiente dirección URL:
  
    [http://www.microsoft.com/windowsxp/pro/techinfo/  
    administration/wirelesssecurity/](http://www.microsoft.com/windows/windows-xp/default.aspx)
  
(Este artículo contiene referencias a guías de otros productos y vínculos a sitios Web que sólo están disponibles en inglés.)
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Apéndice C: Versiones de sistemas operativos compatibles
  
La siguiente tabla muestra el estado de las distintas versiones de cliente y servidor de los sistemas operativos de Microsoft® Windows®. La tabla enumera la función del sistema en esta solución, distintas versiones de los sistemas operativos que pueden utilizarse para esa función y el estado de compatibilidad de cada sistema operativo. La columna final incluye notas explicativas adicionales o advertencias.
  
**Tabla C.1. Estado de compatibilidad con la solución de versiones de sistemas operativos**

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Función</th>
<th style="border:1px solid black;" >Versión del sistema operativo</th>
<th style="border:1px solid black;" >Estado de compatibilidad</th>
<th style="border:1px solid black;" >Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Cliente inalámbrico</td>
<td style="border:1px solid black;">Windows® XP con Service Pack 1 (Professional Edition y Tablet Edition)</td>
<td style="border:1px solid black;">Solución probada</td>
<td style="border:1px solid black;"><br />
</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><br />
</td>
<td style="border:1px solid black;">Pocket PC 2003</td>
<td style="border:1px solid black;">Solución probada</td>
<td style="border:1px solid black;">La implementación de la compatibilidad con WLAN de 802.1X puede variar entre los distintos proveedores del dispositivo Pocket PC.
Microsoft aún no tiene disponible el acceso protegido Wi-Fi (WPA), aunque puede ser compatible con otras compañías.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><br />
</td>
<td style="border:1px solid black;">Windows 2000</td>
<td style="border:1px solid black;">Compatible</td>
<td style="border:1px solid black;">Necesita obtener un cliente 802.1X de Microsoft.com.
La compatibilidad con WPA aún no está disponible desde Microsoft, aunque sí puede estarlo desde otras compañías.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><br />
</td>
<td style="border:1px solid black;">Microsoft Windows NT® 4.0
-Windows 9x</td>
<td style="border:1px solid black;">Compatible</td>
<td style="border:1px solid black;">Necesita obtener un cliente 802.1X a través de Premier Support.
La compatibilidad con WPA aún no está disponible desde Microsoft, aunque sí puede estarlo desde otras compañías.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><br />
</td>
<td style="border:1px solid black;">Otras plataformas</td>
<td style="border:1px solid black;">Desconocido: la compatibilidad puede estar disponible en otras compañías distintas a Microsoft.</td>
<td style="border:1px solid black;">Los clientes necesitan admitir 802.1X y PEAP-MS-CHAP v2.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Entidad emisora de certificados</td>
<td style="border:1px solid black;">Windows Server™ 2003, Standard Edition</td>
<td style="border:1px solid black;">Solución probada</td>
<td style="border:1px solid black;"><br />
</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><br />
</td>
<td style="border:1px solid black;">Windows Server 2003, Enterprise Edition</td>
<td style="border:1px solid black;">Compatible</td>
<td style="border:1px solid black;">Enterprise Edition es un superconjunto de Standard Edition.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><br />
</td>
<td style="border:1px solid black;">Windows 2000 Server</td>
<td style="border:1px solid black;">Compatible</td>
<td style="border:1px solid black;">Las características de la entidad emisora de certificados de Windows 2000 Server son muy parecidas a las de Windows Server 2003, Standard Edition.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><br />
</td>
<td style="border:1px solid black;">Entidades emisoras de certificados de compañías distintas a Microsoft</td>
<td style="border:1px solid black;">Desconocido</td>
<td style="border:1px solid black;">La entidad emisora de certificados debe poder crear certificados de servidor para el Servicio de autenticación de Internet (IAS). Tiene que administrar manualmente la inscripción y renovación.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servidor RADIUS</td>
<td style="border:1px solid black;">Windows Server 2003, Standard Edition</td>
<td style="border:1px solid black;">Solución probada</td>
<td style="border:1px solid black;">Standard Edition sólo admite 50 puntos de acceso inalámbrico como máximo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><br />
</td>
<td style="border:1px solid black;">Windows Server 2003, Enterprise Edition</td>
<td style="border:1px solid black;">Compatible</td>
<td style="border:1px solid black;">Enterprise Edition constituye un superconjunto de Standard Edition. Por tanto, ambas ediciones contienen todas las características requeridas por la solución.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><br />
</td>
<td style="border:1px solid black;">Windows 2000 Server</td>
<td style="border:1px solid black;">Compatible</td>
<td style="border:1px solid black;">El Servicio de autenticación de Internet (IAS) de Windows 2000 se puede utilizar para 802.1X inalámbrico con PEAP. Requiere la instalación de un cliente 802.1X con Windows 2000 en el servidor IAS. No dispone de asistente para la configuración de la directiva de acceso remoto.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><br />
</td>
<td style="border:1px solid black;">Otras plataformas</td>
<td style="border:1px solid black;">Incompatible</td>
<td style="border:1px solid black;"><br />
</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Controladores de dominio</td>
<td style="border:1px solid black;">Windows Server 2003</td>
<td style="border:1px solid black;">Solución probada</td>
<td style="border:1px solid black;">Los grupos universales necesitan el dominio de Active Directory® para el modo nativo de Windows 2000 o posterior.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><br />
</td>
<td style="border:1px solid black;">Windows 2000 Server</td>
<td style="border:1px solid black;">Compatible</td>
<td style="border:1px solid black;">Los grupos universales necesitan el dominio de Active Directory® para el modo nativo de Windows 2000 o posterior.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servidores de infraestructura, Sistema de nombres de dominio (DNS) y Protocolo de configuración dinámica de host (DHCP)</td>
<td style="border:1px solid black;">Windows Server 2003</td>
<td style="border:1px solid black;">Solución probada</td>
<td style="border:1px solid black;"><br />
</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><br />
</td>
<td style="border:1px solid black;">Windows 2000 Server</td>
<td style="border:1px solid black;">Compatible</td>
<td style="border:1px solid black;"><br />
</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><br />
</td>
<td style="border:1px solid black;">Otras plataformas</td>
<td style="border:1px solid black;">Desconocido</td>
<td style="border:1px solid black;">DHCP, DNS y las soluciones de administración proporcionadas por compañías distintas a Microsoft deben funcionar con esta solución, siempre y cuando reúnan los requisitos básicos de los clientes Windows y Active Directory.</td>
</tr>
</tbody>
</table>
  
El estado de compatibilidad que aparece en la tabla se enumera como uno de los siguientes:
  
-   **Solución probada:** la versión del sistema operativo se ha probado específicamente para funcionar como parte de la solución. Las versiones de los productos incluidas en esta categoría también se hallan incluidas en la siguiente categoría ("Compatible").
  
-   **Compatible:** el grupo de productos de Microsoft Windows ha probado esta versión de sistema operativo y Microsoft admite completamente su utilización en esta configuración (aunque es posible que deba proporcionar configuración o personalización adicional además de lo incluido en la guía de esta solución). No obstante, esta versión no se ha probado como parte de esta solución, lo que puede significar que la guía no incluya todos los detalles sobre la instalación y configuración de dicha versión.
  
-   **Incompatible:** la versión del sistema operativo no funcionará con la solución tal y como se describe. Probablemente se pueda configurar el sistema incompatible para que funcione correctamente, pero puede suponer una cantidad de esfuerzo considerable.
  
-   **Desconocido:** la versión del sistema operativo puede funcionar en esta función, puesto que no existe razón técnica para que no sea así. No obstante, es su responsabilidad comprobarlo y probarlo.
  
    **Nota:** en la tabla aparecen varias filas en las que no se relaciona ninguna versión de sistema operativo (en la columna Versión de sistema operativo) con funciones (en la columna Función). En estos casos, o bien el sistema operativo no funciona para esa función (estado **Incompatible**), o no se sabe si funcionará (estado **Desconocido**).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Apéndice D: Secuencias de comandos y archivos auxiliares
  
[](#edaag)[Introducción](#edaag)  
[](#ecaag)[Lista de archivos en la solución](#ecaag)  
[](#ebaag)[Estructura de las secuencias de comandos](#ebaag)
  
### Introducción
  
Este apéndice contiene una breve descripción de las secuencias de comandos y otros archivos auxiliares que se ofrecen con la solución. Aunque son completamente funcionales y se han probado con la solución, las secuencias de comandos no han seguido un proceso de control de calidad exhaustivo. Están especialmente indicadas para ilustrar las técnicas y ofrecer una base para crear sus propias secuencias de comandos administrativas. Se recomienda probar plenamente las secuencias de comandos en su entorno antes de implementarlas en la producción.
  
#### Renuncia
  
Las secuencias de comandos de ejemplo no son compatibles con ningún programa o servicio de soporte estándar de Microsoft®. Las secuencias de comandos de ejemplo se proporcionan TAL CUAL, sin garantía de ningún tipo. Microsoft renuncia a cualquier tipo de garantía implícita, incluidas, pero sin limitarse a, garantías implícitas de comerciabilidad o idoneidad para un determinado fin. El riesgo que resulta del uso o la ejecución de las secuencias de comandos de ejemplo y la documentación es su responsabilidad. En ningún caso, Microsoft, sus autores o aquellos implicados en la creación, producción o entrega de las secuencias de comandos serán responsables por daños de ningún tipo (incluidos, pero sin limitarse a, daños por pérdida de beneficios, interrupción de negocios, pérdida de información comercial o cualquier otra pérdida pecuniaria) que pudiere surgir del uso o la imposibilidad de uso de las secuencias de comandos o la documentación, aún en el caso de que se hubiera informado a Microsoft de la posible ocurrencia de dichos daños.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Lista de archivos en la solución
  
En la tabla siguiente se incluyen todos los archivos que se proporcionan con la solución. Se instalan desde el archivo instalador MSSWLANTools.msi Windows®.
  
**Tabla D.1. Lista de archivos proporcionados con la solución**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de archivo</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Archivos CMD principales</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MSSSetup.cmd
MSSTools.cmd</td>
<td style="border:1px solid black;">Éstos son los archivos por lotes que proporcionan la interfaz con los archivos de Microsoft Windows Scripting Host (WSH) y simplifican la sintaxis. Permiten ejecutar distintos trabajos especificando el nombre del trabajo como un solo parámetro en la línea de comandos. La sintaxis es la siguiente:
<strong>msssetup</strong> <em>NombreTrabajo</em> [/param:<em>valor</em>]
<strong>msstools</strong> <em>NombreTrabajo</em> [/param:<em>valor</em>]
Donde <em>NombreTrabajo</em> es el nombre de la operación. Si ejecuta esta secuencia de comandos sin un NombreTrabajo, todos los trabajos disponibles aparecerán con una descripción sencilla de la función de cada trabajo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Archivos WSH XML</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">msssetup.wsf
msstools.wsf</td>
<td style="border:1px solid black;">Éstos son archivos WSH XML, que especifican los trabajos individuales disponibles. Los trabajos definidos en los archivos WSF llaman a los procedimientos definidos en los archivos VBS. La sintaxis es la siguiente:
<strong>Cscript //job:</strong> <em>NombreTrabajo</em> msstools.wsf [/param:<em>valor</em>]
Si ejecuta esta secuencia de comandos sin un NombreTrabajo, todos los trabajos disponibles en el archivo WSF aparecerán con una descripción sencilla de la función de cada trabajo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Archivos VBScript</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ias_setup.vbs</td>
<td style="border:1px solid black;">Rutinas utilizadas durante la configuración del Servicio de autenticación de Internet (IAS).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ias_tools.vbs</td>
<td style="border:1px solid black;">Rutinas utilizadas durante la operación y la supervisión del IAS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Gen_setup.vbs</td>
<td style="border:1px solid black;">Rutinas que no son específicas de IAS o los Servicios de Certificate Server y que se han utilizado durante la implementación.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ca_setup.vbs</td>
<td style="border:1px solid black;">Rutinas utilizadas durante la configuración de la entidad emisora de certificados.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ca_monitor.vbs</td>
<td style="border:1px solid black;">Rutinas utilizadas por las funciones de supervisión de la entidad emisora.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">constants.vbs</td>
<td style="border:1px solid black;">Constantes utilizadas por los otros archivos VBS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">helper.vbs</td>
<td style="border:1px solid black;">Rutinas genéricas utilizadas por los otros archivos VBS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">pkiparams.vbs</td>
<td style="border:1px solid black;">Constantes utilizadas para definir muchos de los parámetros de configuración de la entidad emisora.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Archivos varios</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">InstCAPICOM.cmd</td>
<td style="border:1px solid black;">Archivo CMD para simplificar la instalación de CAPICOM.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CreateShortCut.cmd</td>
<td style="border:1px solid black;">Archivo CMD que llama a una rutina desde el archivo VBS para crear un acceso directo en el escritorio del usuario. El acceso directo inicia CMD.EXE con el directorio actual en la carpeta de instalación de la secuencia de comandos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ComputerCerts.msc</td>
<td style="border:1px solid black;">Consola de administración predefinida para ver los certificados en el almacén de equipos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">AddRADIUSClient.exe</td>
<td style="border:1px solid black;">Utilidad para agregar clientes de RADIUS a IAS desde la línea de comandos. (<strong>Nota:</strong> esta herramienta requiere la instalación de .NET Framework.)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Interop.SDOIASLib.dll</td>
<td style="border:1px solid black;">Biblioteca de compatibilidad que necesita AddRADIUSClient.exe.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Fuente</td>
<td style="border:1px solid black;">Carpeta que contiene el código fuente de la herramienta AddRADIUSClient.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Archivos de directiva de grupo</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MSSWLANGPOs</td>
<td style="border:1px solid black;">Esta carpeta contiene el archivo de definición XML y los archivos de datos de los dos objetos de directiva de grupo predefinidos que se proporcionan con esta solución.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Documentos</strong></td>
<td style="border:1px solid black;"> </td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Securing Wireless LANs.rtf</td>
<td style="border:1px solid black;">Archivo Léame que contiene el mismo texto que este capítulo.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Estructura de las secuencias de comandos
  
Los archivos de Microsoft Visual Basic® Scripting Edition (VBScript) requieren algunas explicaciones para entender su funcionamiento conjunto. A diferencia de muchos ejemplos de VBScript, los archivos de secuencias de comandos que se incluyen en esta solución contienen varias funciones, a menudo independientes. Para proporcionar acceso a las distintas funciones, estas secuencias de comandos utilizan la funcionalidad de "trabajo" de WSH. De esta forma, un mismo archivo puede contener varias funciones de programa independientes, a las que se llama especificando un nombre de trabajo como parámetro en la secuencia de comandos.
  
Hay dos archivos Windows Script (.wsf), que contienen la interfaz de usuario con todas las operaciones de secuencia de comandos. Los archivos .wsf llaman a un conjunto de archivos .vbs que contienen el código que se utiliza realmente en un trabajo determinado.
  
Puede llamar al trabajo utilizando la siguiente sintaxis:
  
**cscript //job:** *NombreTrabajoArchivoWScript*.wsf
  
Donde *NombreTrabajo* es el nombre de la operación y *ArchivoWScript* es el nombre del archivo de interfaz XML de la secuencia de comandos. A continuación se proporciona un extracto de uno de los archivos .wsf, donde se ha definido el trabajo ConfigureCA:
  
```  
 &lt;?xml version="1.0" encoding="utf-8" ?&gt; &lt;package xmlns="Windows Script Host"&gt; &lt;job id="ConfigureCA"&gt; &lt;description&gt;Configures the CA registry parameters&lt;/description&gt; &lt;script language="VBScript" src="constants.vbs" /&gt; &lt;script language="VBScript" src="pkiparams.vbs" /&gt; &lt;script language="VBScript" src="helper.vbs" /&gt; &lt;script language="VBScript" src="ca\_setup.vbs" /&gt; &lt;script language="VBScript"&gt; &lt;!\[CDATA\[ Initialize True, True ConfigureCA CloseDown \]\]&gt; &lt;/script&gt;   
```  
En este extracto, la definición de trabajo especifica que los archivos .vbs denominados constants.vbs, pkiparams.vbs, helper.vbs y ca\_setup.vbs contienen funciones, subrutinas o datos necesarios para este trabajo; por lo tanto, se deberán cargar. La última sección especifica las funciones de nivel superior que se ejecutan para iniciar el trabajo; en este caso, estas funciones incluyen Initialize (que configura el registro), ConfigureCA (que realiza el trabajo principal de configurar la entidad emisora) y CloseDown (que cierra el registro).
  
En cada uno de los archivos .wsf, el primer trabajo se define para enumerar los nombres (Id.) y las descripciones de todos los trabajos contenidos en el archivo. De esta forma, si se ejecuta el archivo .wsf sin solicitar un trabajo específico, se ejecuta este trabajo predeterminado y aparece una pequeña pantalla de ayuda con los nombres y descripciones de todos los trabajos disponibles en el archivo. En la tabla siguiente se incluyen los trabajos disponibles en cada uno de los archivos .wsf que se proporcionan con la solución.
  
**Tabla D.2. Lista de trabajos en MSSSetup.wsf**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre del trabajo</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">ListJobs</td>
<td style="border:1px solid black;">Enumera todos los trabajos del archivo WSF.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ConfigureCA</td>
<td style="border:1px solid black;">Configura los parámetros del Registro de la entidad emisora.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ConfigureTemplates</td>
<td style="border:1px solid black;">Configura las plantillas de certificado de entidad emisora.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CheckCAEnvironment</td>
<td style="border:1px solid black;">Comprueba el entorno antes de instalar la entidad emisora.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">InstallCA</td>
<td style="border:1px solid black;">Instala los Servicios de Certificate Server.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CreateShortcut</td>
<td style="border:1px solid black;">Crea un acceso directo a <strong>MSS WLAN Tools</strong> en el escritorio.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ImportSecurityGPO</td>
<td style="border:1px solid black;">Importa al dominio un objeto de directiva de grupo con la configuración de seguridad del servidor.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ImportAutoEnrollGPO</td>
<td style="border:1px solid black;">Importa al dominio un objeto de directiva de grupo con la configuración de inscripción automática de certificados.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ImportWLANClientGPO*</td>
<td style="border:1px solid black;">Importa el objeto de directiva de grupo de la configuración de la WLAN.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CheckDomainNativeMode</td>
<td style="border:1px solid black;">Comprueba si el dominio está en modo nativo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">VerifyCAInstall</td>
<td style="border:1px solid black;">Comprueba que la instalación de la entidad emisora ha sido satisfactoria.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">VerifyCAConfig</td>
<td style="border:1px solid black;">Comprueba que la configuración de la entidad emisora ha sido satisfactoria.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">CheckIASEnvironment</td>
<td style="border:1px solid black;">Comprueba el entorno antes de instalar IAS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">InstallIAS</td>
<td style="border:1px solid black;">Instala los Servicios de autenticación de Internet en el servidor.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">CreateWLANGroups</td>
<td style="border:1px solid black;">Crea grupos de seguridad en Active Directory®.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">AddWLANGroupMembers</td>
<td style="border:1px solid black;">Rellena los grupos de seguridad con los miembros correctos.</td>
</tr>
</tbody>
</table>
  
**Nota:** los trabajos marcados con un asterisco (\*) no se utilizan en esta solución.
  
**Tabla D.3. Lista de trabajos en MSSTools.wsf**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre del trabajo</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">ListJobs</td>
<td style="border:1px solid black;">Enumera todos los trabajos del archivo WSF.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">AddRADIUSClient</td>
<td style="border:1px solid black;">Procedimiento interactivo para agregar un cliente de RADIUS a IAS (parámetros: [/path:<em>NombreArchivoSalida</em>]).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">AddSecRADIUSClients</td>
<td style="border:1px solid black;">Procedimiento interactivo para agregar un cliente de RADIUS a IAS (parámetros: [/path:<em>NombreArchivoEntrada</em>]).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">GenRADIUSPwd</td>
<td style="border:1px solid black;">Genera una entrada y un secreto de cliente de RADIUS (parámetros: /client:<em>NombreCliente</em> /ip:<em>DirecciónIPCliente</em> [/path:<em>ArchivoSalida</em>]).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ExportIASSettings</td>
<td style="border:1px solid black;">Exporta una configuración de servidor IAS a los archivos (parámetros: [/path:<em>CarpetaParaGuardarArchivosConfiguración</em>]).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ImportIASSettings</td>
<td style="border:1px solid black;">Importa una configuración de servidor IAS de los archivos (parámetros: [/path:<em>CarpetaConArchivosParaImportar</em>]).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ExportIASClients</td>
<td style="border:1px solid black;">Exporta clientes de RADIUS de IAS al archivo (parámetros: [/path:<em>CarpetaParaGuardarArchivoClientes</em>]).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ImportIASClients</td>
<td style="border:1px solid black;">Importa clientes de RADIUS de IAS del archivo (parámetros: [/path:<em>CarpetaConArchivoClientesParaImportar</em>]).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">BackupIAS</td>
<td style="border:1px solid black;">Hace una copia de seguridad de la configuración de IAS en el archivo (parámetros: [/path:<em>CarpetaParaGuardarArchivoCopiaSeguridad</em>]).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">RestoreIAS</td>
<td style="border:1px solid black;">Restaura la configuración de IAS del archivo (parámetros: [/path:<em>ArchivoCarpetaParaRestaurar</em>]).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">CheckIAS</td>
<td style="border:1px solid black;">Comprueba que el servidor IAS está respondiendo (parámetros: [/verbose]).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CheckCA</td>
<td style="border:1px solid black;">Comprueba que el servicio de entidad emisora está respondiendo y que la lista de revocación de certificados (CRL) es válida (parámetros: [/verbose]).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">EnableIASLockout*</td>
<td style="border:1px solid black;">Habilita el bloqueo de cuentas de IAS (parámetros: [/maxdenials:<em>10</em>] [/lockouttime:<em>2880</em> (seg.)]).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">DisableIASLockout*</td>
<td style="border:1px solid black;">Deshabilita el bloqueo de cuentas de IAS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ShowLockedOutAccounts*</td>
<td style="border:1px solid black;">Muestra las cuentas bloqueadas (y las cuentas con autorizaciones erróneas).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ResetLockedOutAccount*</td>
<td style="border:1px solid black;">Restablece una cuenta bloqueada (parámetros: /account:<em>NombreDominio:NombreCuenta</em>).</td>
</tr>
</tbody>
</table>
  
**Nota:** los trabajos marcados con un asterisco (\*) no se utilizan en esta solución.
  
#### Salida del trabajo
  
La mayoría de las secuencias de comandos registran información de progreso en una ventana de la consola y, en muchos casos, también en un archivo de registro. Esta información puede incluir información de errores si la secuencia de comandos encuentra problemas durante la ejecución. Las secuencias de comandos de supervisión son la excepción a esta regla, ya que están diseñadas para ejecutarse como trabajos programados no interactivos y no envían ninguna salida a la ventana de la consola.
  
Las secuencias de comandos utilizan una ventana desplegable sencilla para mostrar la salida. Al finalizar cada secuencia de comandos, debe elegir si desea mantener abierta la ventana (para consultas futuras) o cerrarla.
  
En la mayoría de los procedimientos de configuración, la salida también se registra en un archivo denominado %SystemRoot%\\debug\\MSSWLAN-Setup.log. La mayoría de las tareas operativas regulares no se registran; no obstante, sí se registran las tareas que puedan tener un efecto significativo en la seguridad o en las operaciones como, por ejemplo, la importación de la configuración de IAS. Las tareas que puedan provocar la escritura de información confidencial en el registro como, por ejemplo, la agregación de clientes de RADIUS y la generación de secretos de clientes de RADIUS, no se registran.
  
#### Ejecución de los trabajos
  
Aunque las secuencias de comandos se pueden ejecutar directamente, existen dos archivos por lotes de shell de comandos (.cmd) que ayudan a simplificar la sintaxis.
  
La sintaxis para ejecutar los archivos .wsf directamente es la siguiente:
  
**Cscript //job:** *NombreTrabajo* MssSetup.wsf
  
En su lugar, puede utilizar los archivos .cmd con la siguiente sintaxis más sencilla:
  
**MssSetup** *NombreTrabajo*
  
Si ejecuta el archivo .cmd sin especificar un trabajo, se ejecuta el primer trabajo (ListJobs) del archivo .wsf; este trabajo enumera los Id. y las descripciones de cada uno de los trabajos del archivo .wsf.
  
Algunos trabajos necesitan también parámetros adicionales. La sintaxis para ejecutar estos trabajos y la información sobre estos parámetros adicionales se describen en los capítulos correspondientes de esta solución. La sintaxis general para especificar parámetros adicionales es:
  
**MssSetup** *NombreTrabajo* /NombreParám:*ValorParám*
  
*NombreParám* es el nombre del parámetro (por ejemplo, "ruta" o "cliente") y *ValorParám* es el valor de ese parámetro (por ejemplo, "C:\\MiArchivo.txt" o "MiEquipo"). Los valores de parámetros que incluyan espacios deben ir entre comillas (").
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Introducción: Elección de una estrategia para la seguridad en LAN inalámbricas
  
[](#efaaz)[Introducción](#efaaz)  
[](#eeaaz)[Motivos para decantarse por las redes inalámbricas](#eeaaz)  
[](#edaaz)[Protección real de la WLAN](#edaaz)  
[](#ecaaz)[Selección de las opciones de WLAN correctas](#ecaaz)  
[](#ebaaz)[Resumen](#ebaaz)  
[](#eaaaz)[Referencias](#eaaaz)
  
### Introducción
  
La tecnología de red de área local inalámbrica (WLAN) constituye un tema controvertido. Las organizaciones que han implementado WLAN están preocupadas acerca de si son o no seguras; a las que no las han implementado aún les preocupa desaprovechar la oportunidad de aumentar la productividad del usuario y reducir costes de propiedad. Existe todavía una gran confusión en relación con la seguridad de una WLAN en el entorno informático corporativo.
  
Desde que se detectaron los puntos débiles en la seguridad de WLAN de primera generación, analistas y empresas dedicadas a la seguridad en las redes han procurado resolver estos problemas. Algunos de estos esfuerzos han contribuido de manera significativa a la causa de la seguridad inalámbrica. Otros han participado de los defectos: algunos introducen un conjunto distinto de vulnerabilidades de seguridad; otros precisan hardware propietario costoso; y otros evitan la cuestión de la seguridad de WLAN por completo protegiéndose con otra tecnología de seguridad potencialmente compleja como es la de las redes privadas virtuales (VPN).
  
Paralelamente, el Instituto de ingenieros eléctricos y electrónicos (IEEE), junto con otros organismos normativos y consorcios, han vuelto a definir y han mejorado con diligencia los estándares de seguridad inalámbrica para permitir que las WLAN hagan frente al entorno de seguridad hostil de principios del siglo veintiuno. Gracias a los esfuerzos de los organismos normativos y los líderes del sector, las palabras "seguridad WLAN" han dejado de ser contradictorias. Las WLAN pueden implementarse y utilizarse actualmente con un gran nivel de confianza en su seguridad.
  
En este documento se presentan dos soluciones de seguridad de WLAN de Microsoft®, así como las preguntas y respuestas acerca de si las WLAN pueden ser seguras y cuál es la mejor manera de protegerlas.
  
#### Descripción general de las soluciones inalámbricas
  
El principal objetivo de este documento es ayudarle a decidir cuál es el método más adecuado para proteger las WLAN de su organización. Para ello, el documento aborda cuatro áreas principales:
  
-   Motivos para decantarse por las WLAN (y las preocupaciones de seguridad asociadas).
  
-   Utilización de los estándares de WLAN seguras.
  
-   Estrategias alternativas, tales como VPN y seguridad del protocolo Internet (IPSec).
  
-   Selección de las opciones de WLAN correctas.
  
Microsoft ha elaborado dos soluciones WLAN, basadas en los estándares abiertos de organismos tales como el IEEE, el Grupo de trabajo de ingeniería de Internet (IETF) y la Alianza Wi-Fi. Estas dos soluciones son: *Solución de Seguridad de LAN inalámbricas — Servicios de Certificate Server de Microsoft Windows Server 2003* y *Seguridad en LAN inalámbricas con PEAP y contraseñas*. Como sus propios nombres indican, la primera utiliza certificados de clave pública para autenticar equipos y usuarios en la WLAN mientras que la segunda recurre simplemente a los nombres de usuario y las contraseñas. No obstante, la arquitectura básica de las dos soluciones es muy similar. Ambas se basan en la infraestructura de Microsoft Windows® Server™ 2003 y los clientes Microsoft Windows XP y Microsoft Pocket PC 2003.
  
Aunque no se deduzca de sus nombres, el público al que están destinadas estas soluciones difiere. *Solución de Seguridad de LAN inalámbricas — Servicios de Certificate Server de Microsoft Windows Server 2003* está orientada sobre todo a organizaciones de gran tamaño con entornos de tecnología de la información (TI) relativamente complejos; mientras que *Seguridad en LAN inalámbricas con PEAP y contraseñas* es una solución bastante más sencilla y se puede implementar con facilidad en organizaciones mucho más pequeñas.
  
Esto no quiere decir que la autenticación de contraseñas no se pueda utilizar en el caso de organizaciones de gran tamaño (o que la autenticación de certificados no sea adecuada para organizaciones más pequeñas), sólo se trata de reflejar el tipo de organización donde es más probable que se utilice esa tecnología en particular. La siguiente ilustración muestra un árbol de decisión sencillo que le ayuda a seleccionar la solución adecuada para su organización. Las tres opciones principales disponibles son:
  
-   El acceso protegido Wi-Fi (WPA) con clave compartida previamente (PSK) dirigida a empresas muy pequeñas u oficinas domésticas.
  
-   Seguridad de WLAN basada en contraseñas para organizaciones que no utilizan ni necesitan certificados.
  
-   Seguridad de WLAN basada en certificados para organizaciones que necesitan y pueden implementar certificados.
  
Estas opciones se explicarán más adelante en este documento, ya que es posible combinar las características de las dos últimas opciones para elaborar una solución híbrida.
  
[![](images/Dd162271.PEAP_i01(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_i01_big(es-es,technet.10).gif)
  
**Figura 1. Árbol de decisión para las soluciones de WLAN de Microsoft**
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Motivos para decantarse por las redes inalámbricas
  
No resulta difícil comprender el atractivo que presentan las WLAN para las empresas de hoy en día. La tecnología WLAN se ha respirado en el ambiente de una u otra forma durante cerca de una década, pero curiosamente no ha conseguido hacer mella hasta hace poco. Sólo cuando la tecnología confiable, estandarizada y de bajo coste se ha encontrado con un interés creciente por disponer de métodos más flexibles de trabajo y una conectividad cada vez más omnipresente, se ha hecho realidad la auténtica adopción de la WLAN. No obstante, la adopción rápida de esta tecnología también ha sacado a la luz una serie de puntos débiles en cuanto a seguridad muy graves, con respecto a la primera generación de WLAN. En este apartado se tratarán los pros (funcionalidad) y los contras (seguridad) de las WLAN.
  
#### Ventajas de las LAN inalámbricas
  
Las ventajas de la tecnología WLAN se dividen en dos categorías principales: ventajas empresariales esenciales y ventajas operativas. Las ventajas empresariales esenciales incluyen productividad mejorada de los empleados, procesos empresariales más rápidos y eficaces, y mayor potencial para elaborar funciones corporativas totalmente nuevas. Las ventajas operativas incluyen costes de administración más bajos y un menor gasto de capital.
  
##### Ventajas empresariales esenciales
  
Las ventajas empresariales esenciales de las WLAN derivan de la flexibilidad y la movilidad de la plantilla.
  
El personal se puede alejar de las mesas de trabajo y moverse fácilmente por las oficinas sin perder la conexión con la red. Es muy práctico observar algunos ejemplos sobre cómo un incremento de la movilidad y de la flexibilidad de la red puede beneficiar a las empresas.
  
-   Los trabajadores móviles que se desplazan de unas oficinas a otras y los teletrabajadores que acuden a la oficina se ahorran mucho tiempo y complicaciones si disponen de un acceso transparente a la red de área local (LAN) corporativa. La conexión es prácticamente instantánea y está disponible desde cualquier lugar con cobertura inalámbrica: no es necesario buscar puertos de red ni cables, ni pedir ayuda al personal de TI para que le ayude a conectarse a la red.
  
-   Los trabajadores expertos pueden permanecer en contacto desde cualquier lugar de la empresa. Utilizando el correo electrónico, los calendarios electrónicos y las tecnologías de chat, el personal puede estar conectado incluso cuando asiste a reuniones o trabaja en otro lugar que no sea su escritorio.
  
-   La información en línea está siempre disponible. Ya no será necesario paralizar las reuniones para que alguien salga disparado a buscar un informe sobre las cifras del último mes o la actualización de una presentación. Todo ello puede mejorar significativamente la calidad y productividad de las reuniones.
  
-   También mejora la flexibilidad de la organización. El personal ya no tendrá que estar siempre en sus escritorios, por lo que los cambios de escritorio o incluso de oficinas enteras serán más rápidos y fáciles, según lo requieran las nuevas estructuras de los equipos o los proyectos.
  
-   La integración de nuevos dispositivos y aplicaciones en el entorno de TI corporativo también mejora considerablemente. Dispositivos como los asistentes digitales personales (PDA) y Tablet PC, que hasta hace poco eran poco más que juguetes de los ejecutivos y no formaban parte importante del departamento de TI, estarán mucho más integrados y serán mucho más útiles cuando las organizaciones dispongan de redes inalámbricas. Los trabajadores y los procesos empresariales que antes no se veían afectados por la tecnología de la información se beneficiarán de los equipos, las aplicaciones y los dispositivos inalámbricos, que se podrán utilizar en áreas que hasta ahora no contaban con redes, como fábricas, hospitales, tiendas y restaurantes.
  
Cada organización disfrutará de ventajas distintas; determinar cuáles son relevantes para su organización dependerá de diversos factores tales como la naturaleza de la empresa y el tamaño y la distribución geográfica de la plantilla.
  
##### Ventajas operativas
  
Las principales ventajas operativas de la tecnología de WLAN son la reducción de los costes operativos y de capital, y se pueden resumir del siguiente modo:
  
-   El coste de dotar a los edificios de acceso a la red se reduce considerablemente. Aunque la mayoría de las oficinas dispone de cableado de red, muchos otros lugares de trabajo como fábricas, almacenes y tiendas no lo tienen. Las redes podrán suministrarse en ubicaciones donde el cableado de red no se podría llevar a cabo; por ejemplo, al aire libre, en el mar o incluso en el campo de batalla.
  
-   El tamaño de la red se puede modificar con gran facilidad, en respuesta a los distintos niveles de demanda conforme la organización cambia, incluso a diario si es preciso. Es mucho más sencillo implementar una mayor concentración de puntos de acceso inalámbrico en una ubicación concreta que aumentar el número de puertos de red con cable.
  
-   Ya no será necesario que el capital esté ligado a la infraestructura del edificio: la infraestructura de red inalámbrica se puede trasladar a otros edificios con relativa facilidad, mientras que el cableado por el suelo está permanentemente unido al edificio.
  
#### Preocupaciones en cuanto a la seguridad de las LAN inalámbricas
  
A pesar de todas estas ventajas, una serie de preocupaciones acerca de la seguridad de las WLAN ha frenado su adopción, sobre todo en los sectores más conscientes de la importancia de la seguridad, como son el de las finanzas o los gubernamentales. Aunque parece obvio el riesgo que supone transmitir sin proteger los datos de una red a cualquiera que se encuentre en las cercanías, existe un número sorprendente de WLAN que se han instalado sin ninguna característica de seguridad activada. La mayoría de las empresas han implementado algún tipo de seguridad inalámbrica; no obstante, suele tratarse de características básicas de primera generación, que no ofrecen una protección adecuada según los estándares actuales.
  
Cuando se desarrollaron los primeros estándares para WLAN, IEEE 802.11, la seguridad no constituía un tema tan preocupante como lo es hoy. El nivel y la sofisticación de las amenazas era muy inferior y la adopción de la tecnología inalámbrica estaba todavía dando sus primeros pasos. Es, en ese momento, cuando surge el esquema de la seguridad de las WLAN de primera generación, conocido como privacidad equivalente por cable (WEP). La WEP subestimó las medidas necesarias para "igualar" la seguridad del aire a la seguridad del cable. En contraposición, los métodos de seguridad de WLAN modernos se diseñaron para trabajar en un entorno hostil como el aire donde no existen unos perímetros físicos o de red claros.
  
Es importante distinguir entre la WEP estática de primera generación (que utiliza una contraseña compartida para proteger la red) y los esquemas de seguridad que utilizan el cifrado WEP junto con una administración de claves de cifrado y una autenticación segura. El primero es un esquema de seguridad completo que incluye autenticación y protección de datos y que, en este documento, se denomina "WEP estática". Por otra parte, la WEP dinámica, define sólo el cifrado de datos y el método de integridad empleado como parte de soluciones más seguras que se describirán más adelante en este mismo documento.
  
Los puntos débiles de seguridad descubiertos en la WEP estática implican que las WLAN protegidas por ella son vulnerables a diversos tipos de amenazas. Las herramientas de "auditoría" disponibles de forma gratuita, como Airsnort y WEPCrack, logran que sea posible introducirse con facilidad en redes inalámbricas protegidas por WEP estáticas. Las WLAN que no han sido protegidas se encuentran expuestas obviamente a las mismas amenazas también; la diferencia radica en que se precisan menos conocimientos, tiempo y recursos para llevar a cabo los ataques.
  
Antes de ver cómo funcionan las soluciones de seguridad de las WLAN modernas, merece la pena revisar las principales amenazas a las que se enfrentan las WLAN. Estas amenazas se resumen en la siguiente tabla.
  
**Tabla 1. Principales amenazas para la seguridad de las WLAN**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Amenaza</th>
<th style="border:1px solid black;" >Descripción de la amenaza</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Interceptación (revelación de datos)</td>
<td style="border:1px solid black;">La interceptación de transmisiones de la red puede dar lugar a la revelación de datos confidenciales y de credenciales de usuario sin protección, además de a una posible usurpación de la identidad. Permite también que intrusos expertos recopilen información sobre los entornos de TI y la utilicen para atacar otros sistemas o datos que, de otra forma, no serían vulnerables.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Interceptación y modificación de los datos transmitidos</td>
<td style="border:1px solid black;">Si un atacante logra obtener acceso a la red, puede introducir un equipo falso que intercepte y modifique los datos comunicados entre dos usuarios autorizados.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Imitación</td>
<td style="border:1px solid black;">El acceso directo a la red interna permite que el intruso falsifique datos que parecen legítimos de manera que no sería posible desde fuera de la red, por ejemplo, un mensaje de correo electrónico de un usuario imitado. Los usuarios, incluso los administradores de sistemas, suelen confiar en los elementos originados dentro de la red mucho más que en los que proceden del exterior de la red corporativa.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Denegación del servicio (DoS)</td>
<td style="border:1px solid black;">Un agresor determinado puede activar un ataque de DoS de diversas maneras. Por ejemplo, la interrupción de las señales de radio se puede activar mediante algo tan simple como un microondas. Existen ataques más complejos cuyo objetivo son los protocolos inalámbricos de bajo nivel, y otros menos complejos cuyo objetivo son las redes mediante un gran incremento del tráfico aleatorio en la WLAN.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Carga libre (o robo de recursos)</td>
<td style="border:1px solid black;">Es posible que los intrusos sólo deseen utilizar su red como punto de libre acceso a Internet. Si bien esto no es tan grave como las demás amenazas, hará que, como mínimo, no sólo empeore el nivel de servicio prestado a los usuarios autorizados sino también que puedan introducirse virus y otras amenazas.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Amenazas accidentales</td>
<td style="border:1px solid black;">Algunas características de las WLAN facilitan la aparición de amenazas no intencionadas. Por ejemplo, un visitante autorizado podría iniciar el equipo portátil sin la intención de conectarse a la red, pero se conecta a su WLAN automáticamente. Así, el equipo portátil del visitante se convierte en un punto de entrada de virus en la red. Este tipo de amenaza sólo se da en WLAN desprotegidas.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">WLAN no autorizadas</td>
<td style="border:1px solid black;">Si su empresa no dispone oficialmente de una WLAN, es posible que siga estando bajo la amenaza de las WLAN sin administrar que surjan en su red. El hardware de WLAN adquirido a bajo precio por parte de empleados entusiastas puede abrir vulnerabilidades no intencionadas en su red.</td>
</tr>
</tbody>
</table>
  
Las preocupaciones sobre seguridad en las WLAN, centradas en la WEP estática, han recibido mucha atención por parte de los medios. A pesar del hecho de que existen buenas soluciones de seguridad para combatir estas amenazas, organizaciones de distintos tamaños recelan de las WLAN. Muchas de ellas han detenido su implementación o han prohibido el uso de la tecnología de WLAN por completo. A continuación, se enumeran algunos factores que contribuyen a difundir esta confusión y el error extendido de que las WLAN y la inseguridad de las redes van de la mano:
  
-   Existe una incertidumbre generalizada acerca de qué tecnología WLAN es segura y cuál no lo es. Las empresas desconfían de todas las medidas de seguridad de WLAN después de la serie de defectos encontrados en las WEP estáticas. La desconcertante lista de estándares oficiales y soluciones de propiedad que dicen solucionar los problemas ha ayudado muy poco a aclarar la confusión.
  
-   Inalámbrica equivale a invisible. Para los administradores de la seguridad de la red, no se trata sólo de una cuestión perturbadora desde un punto de vista psicológico, sino que plantea un problema de administración de la seguridad real. Mientras que es posible *ver* cómo un intruso conecta un cable a una red convencional, la intrusión en las WLAN es mucho menos tangible. Las tradicionales paredes y puertas de defensa física de la seguridad, que ayudan a proteger la red con cable, no constituyen protección frente a un atacante "inalámbrico".
  
-   En la actualidad se tiene una mayor conciencia de la necesidad de proteger la información. Las empresas demandan niveles de seguridad mucho mayores para sus sistemas y desconfían de cualquier tecnología que conlleve vulnerabilidades de la seguridad.
  
-   Como corolario de esta creciente toma de conciencia de la seguridad, existe una serie de requisitos legales y normativos que rigen la seguridad de los datos en un número de países y sectores de la industria que sigue en aumento. Uno de los mejores ejemplos que se conocen de este fenómeno es la Ley de portabilidad y responsabilidad de seguros de salud (HIPAA) de 1996, que regula el manejo de historiales sanitarios personales en Estados Unidos.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Protección real de la WLAN
  
Desde el descubrimiento de las vulnerabilidades de seguridad de las WLAN que se han descrito hasta el momento, los principales proveedores de redes, los organismos reguladores y los analistas han centrado gran parte de sus esfuerzos en encontrar soluciones para hacer frente a estos problemas. De esta forma, se han generado una serie de respuestas a las preocupaciones sobre la seguridad de las WLAN. Las principales opciones son:
  
-   No implementar tecnología de WLAN.
  
-   Mantenerse fiel a la seguridad WEP estática 802.11.
  
-   Utilizar VPN para proteger los datos de la WLAN.
  
-   Utilizar IPSec para proteger el tráfico de la WLAN.
  
-   Utilizar la autenticación 802.1X y el cifrado de datos para proteger la WLAN.
  
Estas estrategias se detallan en orden de menor a mayor grado de satisfacción, basándose en una combinación de seguridad, funcionalidad y aprovechamiento; aunque, hasta cierto punto, se trata de un juicio subjetivo. La opción recomendada por Microsoft es la última: utilizar la autenticación 802.1X y el cifrado de WLAN. Este enfoque se tratará en la siguiente sección y entonces, se evaluará con respecto a la lista de las principales amenazas de WLAN que se han identificado con anterioridad (tabla 1). Las principales ventajas e inconvenientes de los demás enfoques también se abordarán más adelante en este documento, después de esta sección.
  
#### Protección de la WLAN mediante la autenticación 802.1X y el cifrado de datos
  
Este enfoque posee muchos puntos positivos para poder recomendarlo (aunque su nombre y el despliegue de términos oscuros no se encuentren entre ellos). Antes de tratar las ventajas de las soluciones basadas en este enfoque, es importante aclarar algunos términos y explicar cómo funciona la solución.
  
##### Comprensión de la seguridad de WLAN
  
La protección de una WLAN implica tres elementos fundamentales:
  
-   Autenticación del usuario (o dispositivo) que se conecta a la red, de manera que se tenga un elevado grado de confianza en quién o qué está intentando conectarse.
  
-   Autorización del usuario o dispositivo que va a utilizar la WLAN para poder controlar quién obtiene acceso a ella.
  
-   Protección de los datos transmitidos en la red de manera que estén a salvo de interceptaciones y modificaciones no autorizadas.
  
Es posible que precise también una función de auditoría junto con estas opciones, aunque la auditoría es principalmente una manera de comprobar y reforzar estos otros tres elementos.
  
###### Autenticación y autorización de la red
  
La seguridad WEP estática se basa en un mero secreto compartido (clave o contraseña) para la autenticación en la WLAN. Todo el que posea esta clave secreta podrá contar con acceso a la WLAN. La WEP estándar original no proporciona ningún método para automatizar la actualización o distribución de estas claves; por lo tanto, resulta extremadamente difícil cambiarlas con regularidad. Los defectos de cifrado en la WEP implican que un atacante puede descubrir las claves WEP estáticas mediante herramientas sencillas.
  
Con el fin de proporcionar un método más sólido de autenticación y autorización, Microsoft y una serie de proveedores han propuesto un marco de seguridad de WLAN mediante el protocolo 802.1X. 802.1X es un estándar del IEEE para realizar la autenticación del acceso a una red y, si se desea, administrar las claves utilizadas para proteger el tráfico. Su uso no se limita a las redes inalámbricas y, de hecho, también se implementan en muchos conmutadores de LAN de categoría superior.
  
El protocolo 802.1X implica al usuario de la red, un dispositivo de acceso a la red (o puerta de enlace) como un punto de acceso inalámbrico y un servicio de autenticación y autorización en forma de servidor RADIUS (Servicio de usuario de acceso telefónico de autenticación remota). El servidor RADIUS desempeña la labor de autenticar las credenciales de los usuarios y de autorizar el acceso de éstos a la WLAN.
  
1X se basa en un protocolo IETF denominado "protocolo de autenticación extensible" (EAP) para llevar a cabo la comunicación de autenticación entre el cliente y el servidor RADIUS (transmitida por el punto de acceso). EAP es un protocolo general para la autenticación que admite diversos métodos de autenticación, basados en contraseñas, certificados digitales o bien otros tipos de credenciales.
  
Puesto que EAP es un método de autenticación conectable, no existe un único tipo de autenticación estándar EAP que se pueda utilizar. Distintos métodos de EAP, con distintos tipos de credenciales y protocolos de autenticación, pueden resultar apropiados en distintas circunstancias. La utilización de métodos de EAP en la autenticación de WLAN se tratará en una sección más adelante.
  
###### Protección de datos de WLAN
  
La autenticación y el acceso a la red 1X constituyen sólo una parte de la solución. El otro componente significativo es la protección del tráfico de redes inalámbricas.
  
Los defectos del cifrado de datos WEP descritos con anterioridad se podrían haber mejorado si la WEP estática hubiera incluido un método para actualizar automáticamente las claves de cifrado con regularidad. Las herramientas para descifrar la WEP estática precisan recopilar entre uno y diez millones de paquetes cifrados con la misma clave. Dado que las claves WEP estáticas permanecen invariables a menudo durante semanas o meses, suele ser fácil para un atacante recopilar esa cantidad de datos. Puesto que todos los equipos de una WLAN comparten la misma clave estática, las transmisiones de datos desde todos los equipos de la WLAN pueden cosecharse para ayudarle a descubrir la clave.
  
Al utilizar una solución basada en 802.1X, se permite que las claves de cifrado se modifiquen con frecuencia. Como parte del proceso de autenticación segura 802.1X, el método de EAP genera una clave de cifrado que es exclusiva de cada cliente. Para evitar los ataques de descifrado WEP (descritos previamente), el servidor RADIUS fuerza con regularidad la generación de claves de cifrado nuevas. Esto permite que se empleen algoritmos de cifrado WEP (encontrados en la mayoría del hardware de WLAN actual) de una manera mucho más segura.
  
###### WPA y 802.11i
  
Aunque la WEP con el cambio dinámico de claves 802.1X resulta segura para la mayoría de los fines prácticos, existe un conjunto de problemas persistentes entre los que se incluyen:
  
-   WEP utiliza una clave estática aparte para las transmisiones globales como los paquetes de difusión. A diferencia de las claves por usuario, la clave global no se renueva con regularidad. Pese a que es poco probable que los datos confidenciales se transmitan mediante difusión, al emplear una clave estática para la transmisión global se ofrece a los atacantes la oportunidad de descubrir información acerca de la red, como por ejemplo, direcciones IP y nombres de usuario y de equipo.
  
-   Los marcos de redes protegidas por WEP poseen una protección de escasa integridad. Mediante las técnicas criptográficas, un atacante puede modificar la información del marco de WLAN y actualizar el valor de comprobación de la integridad del marco sin que el receptor lo detecte.
  
-   A medida que se mejora la velocidad de transmisión de la WLAN y se mejora la capacidad informática y las técnicas criptoanalíticas, las claves WEP deberán renovarse con mayor frecuencia. De esta forma, se depositará una carga inaceptable en los servidores RADIUS.
  
Para afrontar estos problemas, el IEEE está trabajando en un nuevo estándar de seguridad para las WLAN denominado 802.11i; también conocido como "red de seguridad sólida" (RSN). La Alianza Wi-Fi, un consorcio formado por proveedores de fidelidad inalámbrica (Wi-Fi), ha publicado en un estándar del sector denominado "Acceso protegido Wi-Fi" (WPA) lo que es, básicamente, una versión previa del 802.11i. WPA incluye un amplio subconjunto de funciones de 802.11i. Al publicar el WPA, la Alianza Wi-Fi ha podido exigir la adherencia a la WPA de todos los equipos que lleven el logotipo Wi-Fi y ha permitido que los proveedores de hardware de redes de Wi-Fi ofrezcan una opción de alta seguridad estandarizada con anterioridad a la publicación del 802.11i. WPA reúne un conjunto de características de seguridad ampliamente aceptadas como las técnicas más seguras disponibles en la actualidad para proteger las WLAN.
  
WPA incluye dos modos: uno, que emplea 802.1X y la autenticación RADIUS (conocida simplemente como WPA) y otro esquema más sencillo para entornos SOHO que emplea una clave compartida previamente (conocida como WPA PSK). WPA asocia el cifrado seguro con la autenticación fuerte y el mecanismo de autorización de 802.1X. La protección de datos de WPA elimina las vulnerabilidades conocidas de WEP con los siguientes métodos:
  
-   Utilización de una clave de cifrado única para cada paquete.
  
-   Utilización de un vector de inicialización mucho más largo, duplicando de forma eficaz el espacio de clave al agregar 128 bits adicionales de material para claves.
  
-   Adición de un valor de comprobación de integridad de mensaje firmado que no sea vulnerable a la alteración de datos o la suplantación.
  
-   Incorporación de un contador de marcos cifrado para impedir los ataques de reproducción.
  
No obstante, dado que WPA utiliza algoritmos criptográficos similares a los empleados por WEP, se puede implementar en el hardware existente con una sencilla actualización de firmware.
  
El modo PSK de WPA también permite que las pequeñas organizaciones y los trabajadores domésticos utilicen una WLAN de clave compartida carente de las vulnerabilidades de la WEP estática (siempre que la clave compartida previamente que se haya elegido sea lo bastante segura como para evitar meros ataques de adivinación de contraseña). Al igual que la WEP dinámica y el WPA basado en RADIUS, las claves de cifrado individuales se generan para cada cliente inalámbrico. La clave que se ha compartido previamente se emplea como una credencial de autenticación; si dispone de esa clave, entonces tendrá autorización para emplear la WLAN y recibir una clave de cifrado exclusiva con el fin de proteger los datos.
  
802.11i (RSN) le proporcionará niveles de seguridad todavía más elevados para las WLAN, incluida una mejor protección contra los ataques de DoS. Su lanzamiento está previsto para mediados de 2004.
  
###### Métodos de autenticación de EAP
  
El protocolo de autenticación extensible (EAP) tal y como la palabra "extensible" de su nombre implica, es compatible con muchos métodos de autenticación. Estos métodos pueden emplear distintos protocolos de autenticación tales como Kerberos, seguridad de la capa de transporte (TLS) y el protocolo de autenticación por desafío mutuo de Microsoft (MS-CHAP) con una amplia gama de tipos de credenciales como contraseñas, certificados, token de contraseñas de un solo uso y datos biométricos. Aunque, en teoría, cualquier método de EAP puede utilizarse con 802.1X, no todos son adecuados para su uso con WLAN. En especial, el método empleado debe ser adecuado para su uso en un entorno desprotegido y poder generar claves de cifrado.
  
Los métodos de EAP principales para su uso en WLAN son EAP-TLS, EAP protegido (PEAP), túnel de TLS (TTLS) y EAP ligero (LEAP). De estos, tanto PEAP como EAP-TLS son compatibles con Microsoft.
  
**EAP-TLS**
  
EAP-TLS es un estándar de IETF (RFC 2716) y es, probablemente, el de uso más generalizado, tanto en clientes inalámbricos como en servidores RADIUS. Emplea certificados de clave pública para autenticar tanto los clientes inalámbricos como los servidores RADIUS estableciendo una sesión de TLS cifrada entre los dos.
  
**PEAP**
  
PEAP es un método de autenticación en dos fases. En la primera fase se establece una sesión de TLS para el servidor y se permite que el cliente autentique al servidor mediante el certificado digital del servidor. La segunda fase precisa un segundo método de EAP con túnel dentro de la sesión de PEAP para autenticar al cliente en el servidor RADIUS. De esta forma se permite que PEAP utilice una variedad de métodos de autenticación de cliente, que incluyen contraseñas con el protocolo MS-CHAP versión 2 (MS-CHAP 2) y los certificados que emplean EAP-TLS con túnel dentro de PEAP. La seguridad de los tipos de EAP (tales como MS-CHAP 2) no es suficiente para poder ser utilizados sin la protección de PEAP porque serían vulnerables a los ataques de diccionario sin conexión. La compatibilidad con PEAP está muy extendida dentro de la industria y Microsoft Windows XP Service Pack 1 y Pocket PC 2003 cuentan con compatibilidad integrada para PEAP.
  
**TTLS**
  
TTLS es un protocolo de dos fases similar a PEAP que emplea una sesión de TLS con el fin de proteger una autenticación de cliente con túnel. Además de los métodos de EAP con túnel, TTLS también puede utilizar versiones ajenas a EAP de los protocolos de autenticación como CHAP, MS-CHAP y otros. Microsoft y Cisco no admiten TTLS, aunque otros proveedores suministran clientes de TTLS para una serie de plataformas.
  
**LEAP**
  
LEAP es un método de EAP de propiedad desarrollado por Cisco, que emplea contraseñas para autenticar clientes. Pese a estar muy extendido, LEAP sólo funciona con hardware y software de Cisco y algunos proveedores más. LEAP también presenta diversas vulnerabilidades de seguridad tales como propensión a ataques de diccionario sin conexión (que permiten que los atacantes descubran las contraseñas de los usuarios) y los ataques de intermediario. En un entorno de dominio, LEAP sólo puede autenticar al *usuario* en la WLAN, pero no al *equipo*. Sin la autenticación de equipos, las directivas de grupo de equipos no se ejecutarán correctamente, la configuración de instalación del software, los perfiles de itinerancia y las secuencias de comandos de inicio de sesión pueden fallar y no será posible que los usuarios cambien las contraseñas caducadas.
  
Existen soluciones de seguridad para las WLAN que emplean 802.1X junto con otros métodos de EAP. Algunos de estos métodos de EAP, tales como EAP-MD5, presentan puntos débiles significativos en cuanto a seguridad cuando se emplean en un entorno de WLAN, así que no deberían utilizarse nunca. Existen otros que admiten la utilización de tokens de contraseña de un solo uso y otros protocolos de autenticación como Kerberos. Estos siguen teniendo un impacto considerable en el mercado de WLAN.
  
##### Ventajas de 802.1X con la protección de datos de WLAN
  
Las ventajas clave de una solución 802.1X se resumen en la siguiente lista:
  
-   **Nivel de seguridad alto:** se trata de un esquema de autenticación de seguridad elevado porque puede emplear certificados de cliente o nombres de usuario y contraseñas.
  
-   **Cifrado más seguro:** permite un cifrado muy seguro de los datos de la red.
  
-   **Transparencia:** proporciona una autenticación y una conexión a la WLAN transparentes.
  
-   **Autenticación de usuarios y de equipos:** permite la autenticación por separado de usuario y de equipo. La autenticación por separado de un equipo permite administrarlo incluso cuando ningún usuario ha iniciado la sesión.
  
-   **Bajo coste:** bajo coste del hardware de red.
  
-   **Alto rendimiento:** dado que el cifrado se lleva a cabo en el hardware de WLAN y no en la CPU del equipo cliente, el cifrado de WLAN no influirá en el nivel de rendimiento del equipo cliente.
  
La solución 802.1X también cuenta con algunas advertencias.
  
-   Aunque 802.1X disfruta de una aceptación casi universal, el uso de distintos métodos de EAP implica que la interoperabilidad no siempre está garantizada.
  
-   WPA está todavía en las primeras fases de adopción así que es posible que no se encuentre disponible en hardware más antiguo.
  
-   La RSN (802.11i) de próxima generación está todavía pendiente de ratificación y precisará la implantación de actualizaciones de hardware y software (por lo general, el hardware de red necesitará una actualización de firmware).
  
No obstante, éstos son problemas relativamente menores y se ven compensados con facilidad por las ventajas; sobre todo, cuando se comparan con los defectos más graves de los enfoques alternativos que se comentan más adelante.
  
###### Resistencia de la solución 802.1X a las amenazas de la seguridad
  
Las principales amenazas de la seguridad para las WLAN se detallaron con anterioridad en este documento (en la tabla 1). Estas amenazas se vuelven a valorar en la siguiente tabla en comparación con una solución basada en 802.1X y la protección de datos de WLAN.
  
**Tabla 2. Amenazas contra la seguridad valoradas en función de la solución propuesta**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Amenaza</th>
<th style="border:1px solid black;" >Mitigación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Interceptación (revelación de datos)</td>
<td style="border:1px solid black;">La asignación y modificación dinámicas de las claves de cifrado con regularidad y el hecho de que las claves sean exclusivas para cada sesión de usuario implica que siempre y cuando la actualización de la clave se realice con suficiente frecuencia, no se podrán descubrir las claves ni disponer de acceso a los datos de ninguna forma conocida.
WPA ofrece mayor seguridad al cambiar las claves de cifrado por paquete. La clave global (que protege el tráfico de difusión) se cambia por paquete.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Interceptación y modificación de datos transmitidos</td>
<td style="border:1px solid black;">La aplicación de la integridad de datos y el cifrado de datos de alta seguridad entre el cliente inalámbrico y el punto de acceso inalámbrico garantiza que un usuario malicioso no pueda interceptar y modificar los datos en tránsito.
La autenticación mutua entre el cliente, el servidor RADIUS y el punto de acceso inalámbrico hace que sea muy difícil que un atacante pueda suplantar a alguno de ellos.
WPA mejora la integridad de los datos con el protocolo Michael.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Imitación</td>
<td style="border:1px solid black;">La autenticación segura en la red impide que usuarios no autorizados se conecten a la red e introduzcan datos imitados desde el interior.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Denegación de servicio (DoS)</td>
<td style="border:1px solid black;">Los ataques de exceso de datos y otros ataques de DoS en la red se pueden evitar si se controla el acceso a la WLAN mediante 802.1X. No existe defensa contra los ataques de DoS de 802.11 de bajo nivel ya sea WEP dinámica o WPA. Este problema se ha afrontado con el estándar 802.11i.
No obstante, incluso este estándar nuevo no será inmune a la interrupción de la capa física (nivel de radio) de las redes.
Estas vulnerabilidades son una característica de las WLAN 802.11 actuales y común a todas las demás opciones que se tratarán más adelante en este documento.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Carga libre (robo de recursos)</td>
<td style="border:1px solid black;">El requisito de autenticación segura impide la utilización no autorizada de la red.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Amenazas accidentales</td>
<td style="border:1px solid black;">El requisito de autenticación segura impide la conexión accidental a la WLAN.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">WLAN no autorizadas</td>
<td style="border:1px solid black;">Si bien la solución no se ocupa directamente de los puntos de acceso inalámbrico no autorizados, la implementación de una solución inalámbrica segura como ésta elimina, casi por completo, los motivos para establecer una WLAN no oficial.
No obstante, debería planear la creación y publicación de una directiva que prohibiese la utilización de WLAN sin aprobar. Puede aplicar la directiva mediante herramientas de software que exploren la red en busca de direcciones de hardware de puntos de acceso inalámbrico y los equipos portátiles de detección de WLAN.</td>
</tr>
</tbody>
</table>
 

#### Otros enfoques para la seguridad de WLAN

En la sección anterior se trató la autenticación 802.1X con la protección de datos de WLAN con más detenimiento. En esta sección se describirán las cuatro alternativas a la seguridad de WLAN citadas con anterioridad (al comienzo de la sección "Protección real de la WLAN").

Los otros cuatro enfoques enumerados eran:

-   No implementar tecnología de WLAN.

-   Mantenerse fiel a la seguridad WEP estática 802.11.

-   Utilizar VPN para proteger los datos de la WLAN.

-   Utilizar IPSec para proteger el tráfico de la WLAN.

Los factores diferenciadores más importantes entre estos enfoques y una solución basada en 802.1X se resumen en la siguiente tabla (aunque la opción "Sin WLAN" no se incluye puesto que no se puede comparar directamente con las demás). Estas opciones se abordan con más detalle en las secciones siguientes.

**Tabla 3. Comparación de los enfoques de seguridad de WLAN**

 
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Característica</th>
<th style="border:1px solid black;" >WLAN 802.1X</th>
<th style="border:1px solid black;" >WEP estática</th>
<th style="border:1px solid black;" >VPN</th>
<th style="border:1px solid black;" >IPSec</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Autenticación
segura (1)</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">No</td>
<td style="border:1px solid black;">Sí,
pero no las VPN que utilicen autenticación de clave compartida.</td>
<td style="border:1px solid black;">Sí,
si se emplea autenticación de certificados o Kerberos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cifrado de datos de alta seguridad</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">No</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">Sí</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Conexión transparente y reconexión a la WLAN</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">No</td>
<td style="border:1px solid black;">Sí</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Autenticación de usuario</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">No</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">Sí</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Autenticación
de equipo (2)</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">No</td>
<td style="border:1px solid black;">Sí</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Difusión y tráfico de multidifusión protegidos</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Se requieren dispositivos de red adicionales</td>
<td style="border:1px solid black;">Servidores RADIUS</td>
<td style="border:1px solid black;">No</td>
<td style="border:1px solid black;">Servidores VPN, servidores RADIUS</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Acceso seguro a la propia WLAN</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">No</td>
<td style="border:1px solid black;">No</td>
</tr>
</tbody>
</table>
  
(1) Muchas implementaciones de VPN que utilizan el modo de túnel IPSec emplean un esquema de autenticación de clave compartida débil, conocido como XAuth.
  
(2) La autenticación de equipo se refiere a que el equipo permanecerá conectado a la WLAN y a la red corporativa incluso si no hay ningún usuario que haya iniciado la sesión en el equipo. Esta capacidad es necesaria para que las siguientes funciones de dominio de Windows actúen correctamente:
  
-   Perfiles de itinerancia de usuario.
  
-   Configuración de directiva de grupo de equipos (en especial secuencias de comandos de inicio y software implementado).
  
-   Secuencias de comandos de inicio de sesión de usuario y software implementado mediante la directiva de grupo.
  
##### Alternativa 1: No implementar la tecnología WLAN
  
Quizás la manera más evidente de lidiar con las amenazas de la seguridad en las WLAN sea evitarlas por completo al no implementar ninguna WLAN. Además de tener que renunciar a los beneficios de las WLAN esbozados con anterioridad en este documento, esta estrategia no está libre de dificultades. Las organizaciones que siguen este enfoque deben tratar con lo que el grupo META denomina el "precio de la demora", que es más que un mero coste de la oportunidad. El estudio del grupo META basó sus hallazgos en el análisis del método no administrado con el que se desarrolló el uso de las redes locales por cable en muchas organizaciones durante una década. En la mayoría de los casos, los departamentos de TI centrales se vieron obligados a dar el paso y tomar el control de la implementación de la LAN a posteriori. Como suele ocurrir, el coste de volver a implementar las numerosas redes locales de departamentos independientes y, a menudo, incompatibles, fue enorme. Si desea obtener más información, consulte el artículo "How Do I Limit My Exposure Against the Wireless LAN Security Threat? The New Realities of Protecting Corporate Information" publicado por el grupo META el 18 de diciembre de 2002.
  
Ésta es la misma amenaza que ha emergido con las WLAN, sobre todo en empresas grandes donde, con frecuencia, no se puede ver físicamente lo que sucede en cada ubicación. La implementación de bases no administradas de WLAN, posible debido al coste extremadamente bajo de los componentes, es con toda probabilidad la peor situación. De esta forma, las organizaciones quedan expuestas a todas las amenazas de la seguridad descritas con anterioridad, y además, no disponen del grupo de TI central que conoce todo lo necesario acerca de ellas o que es capaz de dar los pasos precisos para combatir las amenazas.
  
Por tanto, si su estrategia es la de no adoptar la tecnología de WLAN, tendrá que llevarla a cabo de forma activa y no pasiva. Debe respaldar esta decisión con una directiva clara publicada y asegurarse de que todos los empleados conocen tanto esta directiva como las consecuencias de no cumplirla. Podría interesarle disponer de equipamiento de exploración y monitores de paquetes de red para detectar el uso no autorizado de equipos inalámbricos en su red.
  
##### Alternativa 2: Utilizar seguridad básica mediante 802.11 (WEP estática)
  
La seguridad 802.11 básica (WEP estática) emplea una clave compartida para controlar el acceso a la red y usa la misma clave para cifrar el tráfico inalámbrico. Este modelo de autorización simple se complementa a menudo con el uso del filtrado de puertos basado en direcciones de hardware de tarjeta de WLAN, aunque no forma parte de la seguridad de 802.11 como tal. El principal atractivo de este enfoque es su sencillez. Si bien ofrece un nivel de seguridad algo mejor que las WLAN sin proteger, cuenta con grandes inconvenientes de administración y seguridad, sobre todo en organizaciones de gran tamaño.
  
Entre los inconvenientes de utilizar WEP se incluyen los siguientes:
  
-   Las claves WEP estáticas se pueden averiguar en cuestión de horas en una red con bastante tráfico si se utiliza un equipo con un adaptador de WLAN y herramientas de pirateo, como Airsnort o WEPCrack.
  
-   El punto débil más grave de WEP es que no existe ningún mecanismo para asignar o actualizar dinámicamente la clave de cifrado de la red. Sin 802.1X ni EAP para aplicar las actualizaciones de clave regulares, el algoritmo de cifrado empleado por la WEP será vulnerable a los ataques de recuperación de claves tal y como se ha descrito con anterioridad.
  
-   Las claves estáticas se pueden cambiar, pero el proceso para hacerlo en los puntos de acceso y los clientes inalámbricos es, por lo general, manual y laborioso. Para empeorar la situación, las actualizaciones de clave se deben efectuar en los clientes y los puntos de acceso simultáneamente con el fin de evitar que se interrumpa la conexión de los clientes. En la práctica, esto resulta tan difícil que las claves se suelen dejar sin modificar.
  
-   La clave estática precisa que se comparta entre todos los usuarios de la WLAN y todos los puntos de acceso inalámbrico. Un secreto compartido entre un gran número de personas y dispositivos es poco probable que permanezca a salvo durante mucho tiempo.
  
WEP proporciona a las WLAN un mecanismo de control del acceso muy limitado, basado en el conocimiento de la clave WEP. Si se descubre el nombre de la red (algo muy sencillo) y la clave WEP, es posible conectarse a la red.
  
Una manera de intentar mejorar esta situación es configurar los puntos de acceso inalámbrico de forma que sólo admitan un conjunto predefinido de direcciones de adaptadores de red cliente. Esto suele conocerse como filtrado de direcciones de control de acceso de medios (MAC). La capa MAC hace referencia al firmware de bajo nivel del adaptador de red.
  
El filtrado de direcciones de adaptadores de red para controlar el acceso conlleva sus propios problemas:
  
-   La facilidad de administración es extremadamente pobre. Mantener una lista de direcciones de hardware de todo menos de un número pequeño de clientes es difícil. Además, distribuir esta lista a todos los puntos de acceso y sincronizarla a través de ellos constituye un reto importante.
  
-   La escalabilidad es escasa. Los puntos de acceso tienen un límite del tamaño de la tabla de filtros finito, lo que restringe el número de clientes que se pueden admitir.
  
-   No hay forma de asociar una dirección de MAC a un nombre de usuario, por lo que sólo se puede autenticar por identidad de equipo y no por identidad de usuario.
  
-   Un usuario malintencionado podría imitar una dirección de MAC "autorizada". Si se puede descubrir una dirección de MAC legítima, resulta muy fácil para un intruso utilizarla en lugar de la predefinida grabada en el adaptador.
  
Las soluciones de claves compartidas previamente sólo resultan prácticas cuando se trata de un número reducido de usuarios y puntos de acceso debido a la dificultad de administrar actualizaciones de claves a través de diversas ubicaciones. Los defectos del cifrado de WEP implican que su utilidad es extremadamente cuestionable, incluso en entornos muy reducidos.
  
No obstante, el modo de claves compartidas previamente de WPA proporciona un buen nivel de seguridad con una carga de infraestructura muy baja para las pequeñas organizaciones. Una amplia gama de hardware es compatible con WPA PSK y los clientes WLAN se pueden configurar manualmente. Debería considerarse la configuración de la elección de entornos SOHO.
  
##### Alternativa 3: Redes privadas virtuales
  
Las VPN son probablemente la manera más popular de cifrado de red; mucha gente confía en las tecnologías de VPN probadas y de confianza para proteger la confidencialidad de los datos enviados a través de Internet. Cuando se detectaron las vulnerabilidades de la WEP estática, VPN se propuso rápidamente como *la* manera de proteger los datos que viajan a través de una WLAN. Algunos analistas, como el Grupo Gartner, promocionaron este enfoque y, lógicamente, los distribuidores de soluciones para VPN lo fomentaron con entusiasmo.
  
VPN es una solución excelente para atravesar una red hostil como Internet (aunque la calidad de las implementaciones de VPN varíe). Sin embargo, no es necesariamente la mejor solución para asegurar las WLAN internas. Para este tipo de aplicaciones, una VPN ofrece poca o ninguna seguridad adicional en comparación con las soluciones 802.1X; al mismo tiempo que incrementan de manera significativa la complejidad y los costes, reducen el aprovechamiento y hacen que partes importantes de las funciones no estén operativas.
  
**Nota:** se distingue de la utilización de VPN para asegurar el tráfico a través de zonas interactivas de la LAN pública inalámbrica. La protección de los datos de red de usuarios que se conectan a través de redes remotas hostiles constituye un uso legítimo de las VPN. En estos escenarios, los usuarios esperan que las conexiones seguras sean más molestas y menos funcionales que las conexiones LAN; algo inesperado dentro de las propias instalaciones de la empresa.
  
Entre las ventajas de utilizar VPN para proteger las WLAN se incluyen:
  
-   La mayoría de las organizaciones ya han implementado una solución de VPN, así que tanto los usuarios como el personal de TI estarán familiarizados con la solución.
  
-   La protección de los datos de la VPN suele emplear el cifrado de software que permite que los algoritmos se modifiquen y se actualicen con mayor facilidad que el cifrado basado en el hardware.
  
-   Es posible utilizar hardware relativamente menos costoso porque la protección de VPN es independiente del hardware de WLAN (aunque el aumento de precio que conlleva el hardware de red apto para 802.1X no ha desaparecido en absoluto).
  
Entre los inconvenientes de utilizar VPN en lugar de la seguridad de WLAN nativa se incluyen:
  
-   Las VPN carecen de transparencia para el usuario. Por regla general, los clientes VPN precisan que el usuario inicie manualmente una conexión con el servidor de VPN; por lo tanto, la conexión nunca será tan transparente como una conexión LAN con cable. Los clientes de VPN ajenos a Microsoft también pueden solicitar credenciales de inicio de sesión al conectarse además del inicio de sesión a la red estándar o al dominio. Si la VPN se desconecta, debido a una señal de WLAN escasa o como consecuencia de que el cliente se esté moviendo entre los puntos de acceso, el usuario deberá volver a conectarse.
  
-   Dado que la conexión de VPN sólo la puede iniciar el usuario, un equipo inactivo o desconectado no se conectará a la VPN (y por lo tanto, tampoco a la LAN corporativa). En consecuencia, un equipo no se puede administrar o supervisar remotamente a menos que un usuario inicie la sesión. Determinadas configuraciones de objeto de directiva de grupo de equipos (GPO), tales como las secuencias de comandos de inicio y el software asignado al equipo, no se aplicarán nunca.
  
-   Es posible que los perfiles de itinerancia, las secuencias de comandos de inicio de sesión y el software implementado para el usuario mediante el GPO no funcionen como se esperaba. A menos que el usuario elija iniciar la sesión mediante la conexión de VPN desde el mensaje de inicio de sesión de Windows, el equipo no se conectará a la LAN corporativa hasta después de que el usuario haya iniciado la sesión y haya iniciado la conexión de VPN. Los intentos anteriores de obtener acceso a la red segura darán error. En el caso de un cliente VPN que no sea de Microsoft, puede ser imposible realizar un inicio de sesión de dominio completo a través de la conexión de VPN.
  
-   Si se reanuda desde un estado de espera o hibernación, la conexión de VPN no se volverá a establecer de forma automática, sino que el usuario deberá hacerlo manualmente.
  
-   Aunque los datos del interior del túnel VPN están protegidos, la VPN no ofrece protección para la propia WLAN. Un intruso podría seguir conectado a la WLAN e intentar sondear o atacar dispositivos conectados a la WLAN.
  
-   Los servidores de la VPN se pueden convertir en un cuello de botella. Todo el acceso de clientes WLAN a la LAN corporativa se realiza a través del servidor. Los dispositivos VPN suelen prestar servicio a una gran cantidad de clientes remotos con velocidades relativamente bajas; de ahí, que la mayoría de las puertas de enlace VPN no puedan hacer frente a las decenas o cientos de clientes que se ejecutan con toda la velocidad de una LAN.
  
-   Los gastos de hardware adicional y de administración continua de los dispositivos de VPN son probablemente muy superiores a los de una solución de WLAN nativa. Cada sitio necesitará, habitualmente, su propio servidor VPN junto con los puntos de acceso de WLAN.
  
-   Las sesiones de VPN son más susceptibles de desconectarse cuando los clientes se mueven entre puntos de acceso. Aunque las aplicaciones admitirán a menudo desconexiones momentáneas al cambiar de un punto de acceso inalámbrico a otro, las sesiones de VPN se interrumpirán con frecuencia y necesitarán que el usuario las vuelva a conectar manualmente.
  
-   El coste del servidor VPN y de las licencias de software del cliente, así como el coste de implementar el software, pueden constituir un problema en el caso de soluciones de VPN ajenas a Microsoft. Es posible también que le preocupe la compatibilidad del software del cliente VPN ya que, a menudo, los clientes que no son de Microsoft sustituyen funciones principales de Windows.
  
-   Muchos analistas y proveedores suponen, sin manifestarlo abiertamente, que la seguridad de las VPN siempre es mejor que la de las WLAN. Aunque esto puede ser cierto en el caso de la WEP estática, no tiene por qué ser necesariamente el caso de las soluciones basadas en EAP 802.1X que se describen en este documento. En especial los métodos de autenticación de VPN son, a menudo, *muy poco* seguros y, en el mejor de los casos, no suelen ser mucho más seguros. Por ejemplo, las soluciones de WLAN compatibles con Microsoft utilizan exactamente los mismos métodos de autenticación de EAP que sus soluciones de VPN (EAP-TLS y MS-CHAP versión 2). Muchas de las implementaciones de VPN, sobre todo las que se basan en el modo de túnel IPSec, emplean la autenticación de claves compartidas previamente (una contraseña de grupo). Ésta se ha desprestigiado ampliamente y se ha mostrado que posee graves vulnerabilidades de seguridad (irónicamente, comparte algunas de estas vulnerabilidades con la WEP estática).
  
-   Una VPN no protege la WLAN propiamente dicha. Aunque los datos del interior de los túneles VPN son seguros, cualquiera puede seguir conectándose a la WLAN e intentando atacar a clientes inalámbricos legítimos u otros dispositivos de la WLAN.
  
VPN se adapta de manera ideal para asegurar el paso del tráfico a través de redes hostiles, tanto si el usuario se ha conectado a través de una conexión de banda ancha doméstica o desde una zona interactiva inalámbrica. No obstante, las VPN nunca se diseñaron para proteger el tráfico de la red en las redes internas. Para la mayoría de las organizaciones, las VPN con este papel serían demasiado voluminosas y estarían limitadas en cuanto a las funciones para el usuario; además de ser demasiado costosas y complejas para el departamento de TI encargado de mantenerlas.
  
En los casos excepcionales donde se precisa seguridad más elevada para una conexión concreta o un tipo de tráfico, dicha seguridad se puede suministrar mediante un túnel VPN o un modo de transporte IPSec *además de* la protección de WLAN nativa. Se trata de la utilización más sensata de los recursos de la red.
  
##### Alternativa 4: Seguridad IP
  
IPSec permite que dos partes de una red se autentiquen la una a la otra de forma segura y autentiquen o cifren paquetes de red individuales. IPSec se puede utilizar tanto para abrir un túnel seguro de una red a otra, como para simplemente proteger los paquetes IP que se transmiten entre dos equipos.
  
Los túneles IPSec se suelen utilizar en el acceso de cliente o las conexiones de VPN de sitio a sitio. El modo de túnel IPSec es una forma de VPN y funciona con la encapsulación de un paquete de IP completo dentro de un paquete protegido mediante IPSec. Esto agrega una carga a la comunicación, al igual que otras soluciones de VPN, que no es realmente necesaria para la comunicación entre sistemas de la misma red. Los pros y los contras del modo de túnel IPSec se han desarrollado en la sección anterior sobre VPN.
  
IPSec también puede asegurar el tráfico de un extremo a otro entre dos equipos (sin túnel) mediante el *modo de transporte* IPSec. Al igual que VPN, IPSec es una solución excelente en muchas circunstancias, si bien, como se aclarará en esta sección, no puede sustituir directamente a la protección de WLAN nativa que se distribuye en la capa de hardware de red.
  
Algunas de las ventajas de la protección del modo de transporte IPSec son:
  
-   Es transparente para los usuarios. Al contrario de las VPN, no se precisa ningún procedimiento de inicio de sesión especial.
  
-   La protección de IPSec es independiente del hardware de WLAN. Sólo precisa una WLAN abierta y sin autenticar. A diferencia de las VPN, no se necesitan servidores ni dispositivos adicionales porque la seguridad se negocia entre los equipos en cada extremo de la comunicación.
  
-   La utilización de algoritmos de cifrado no se encuentra limitada por el hardware de WLAN.
  
Entre los inconvenientes de utilizar IPSec en lugar de la seguridad de WLAN nativa se incluyen:
  
-   IPSec utiliza sólo la autenticación de nivel de equipo y no existe manera de implementar a la vez un esquema de autenticación basado en el usuario. Para muchas organizaciones, esto no supondrá ningún problema pero permite que los usuarios *no autorizados* se conecten a otros equipos protegidos con IPSec de la red si inician la sesión en un equipo *autorizado*.
  
    **Nota:** algunas implementaciones de IPSec en plataformas que no son de Windows utilizan sólo la autenticación de usuario. No obstante, al igual que ocurre con la solución de VPN, el equipo no se conectará a la red cuando el usuario no haya iniciado la sesión; de este modo, impide determinadas operaciones de administración y se desactivan las funciones de la configuración del usuario.
  
-   La administración de directivas IPSec puede ser muy complicada en grandes organizaciones. Si se trata de imponer la protección general del tráfico IP, se podrían poner en peligro otros usos más especializados de IPSec, donde la protección de un extremo a otro es necesaria.
  
-   La seguridad completa exige el cifrado de todo el tráfico de un extremo a otro, pero algunos dispositivos pueden ser incompatibles con IPSec. De este modo, se obligaría a que el tráfico hacia estos dispositivos se transmita sin cifrar. IPSec no ofrecerá protección para estos dispositivos, que quedarán expuestos a todos los usuarios que se conecten a la WLAN.
  
-   Dado que la protección de IPSec se produce en la red en lugar de la capa de MAC, no es totalmente transparente para los dispositivos de red, tales como los servidores de seguridad. Algunas implementaciones de IPSec no funcionarán a través de un dispositivo de traducción de direcciones de red (NAT).
  
-   IPSec de un extremo a otro no puede proteger el tráfico de difusión o multidifusión porque IPSec depende de dos partes que se autentican e intercambian claves mutuamente.
  
-   Aunque los datos del interior de los paquetes IPSec se encuentran protegidos, la propia WLAN no está protegida. Un intruso podría seguir conectándose a la WLAN e intentar sondear o atacar cualquier dispositivo conectado a la WLAN; o bien escuchar el tráfico que no esté protegido con IPSec.
  
-   El cifrado y descifrado de tráfico de la red IPSec carga la CPU del equipo. Esto puede sobrecargar en exceso los servidores utilizados. Aunque esta carga de procesamiento se puede desviar hacia tarjetas de red especializadas, es habitual que no se encuentren integradas de forma predeterminada.
  
Al igual que las VPN, IPSec constituye una solución excelente para muchas situaciones de seguridad pero no afronta la seguridad de la WLAN ni tampoco la protección de WLAN nativa.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Selección de las opciones de WLAN correctas
  
A raíz del debate anterior, debería ser obvio que una solución de WLAN 802.1X es, con diferencia, la mejor opción disponible. Sin embargo y como se indica en la sección "Comprensión de la seguridad de WLAN", una vez que se ha decidido emplear una solución 802.1X, es preciso elegir entre una serie de opciones que conformarán la solución.
  
Las dos elecciones principales son:
  
-   Si se emplean contraseñas o certificados para autenticar los equipos y los usuarios.
  
-   Si se emplea la WEP dinámica o la protección de datos de WLAN de WPA.
  
Estos dos elementos son independientes el uno del otro.
  
Como se comentó con anterioridad en este documento, Microsoft posee dos guías sobre la solución de seguridad de WLAN; una, que emplea autenticación de contraseña y otra, que emplea autenticación de certificados. Estas soluciones funcionan tanto con WEP dinámica como con WPA.
  
#### Decisión de la solución de seguridad para WLAN correcta
  
El siguiente diagrama de flujo resume la elección entre las dos soluciones de seguridad de WLAN.
  
[![](images/Dd162271.PEAP_i02(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162271.peap_i02_big(es-es,technet.10).gif)
  
**Figura 2. Árbol de decisión para las soluciones de seguridad de WLAN**
  
El resultado de este árbol de decisión depende del tamaño y de los requisitos de seguridad específicos de su organización. La mayoría de las organizaciones serán capaces de utilizar una u otra solución de WLAN de Microsoft sin ninguna modificación. Por ejemplo, la mayoría de las empresas, desde pequeñas a medianas, elegirá la solución más sencilla, basada en contraseñas, que se describe en la guía de la solución *Seguridad en LAN inalámbricas con PEAP y contraseñas*. Las empresas más grandes es más probable que se inclinen por la solución basada en certificados digitales: *Solución de Seguridad de LAN inalámbricas — Servicios de Certificate Server de Microsoft Windows Server 2003*.
  
Aunque cada una de las soluciones se desarrolló teniendo en mente dicho público, ambas son muy flexibles. Tanto las empresas que disponen de decenas de usuarios como las que cuentan con varios miles pueden implementar la *Seguridad en LAN inalámbricas con PEAP y contraseñas*. *Solución de Seguridad de LAN inalámbricas — Servicios de Certificate Server de Microsoft Windows Server 2003* se aplica a organizaciones con centenares o decenas de miles de usuarios (las empresas con menos de quinientos usuarios no suelen disponer de suficientes recursos de TI para implementar y mantener las autoridades emisoras de certificados).
  
Un caso muy común y que no se ha tratado directamente en ninguna de las guías es el de las grandes empresas que implementan soluciones de WLAN basadas en contraseñas. Aunque los detalles técnicos de la solución *Seguridad en LAN inalámbricas con PEAP y contraseñas* son igualmente aplicables a las empresas grandes y pequeñas, muchos de los detalles de diseño, programación y funcionamiento necesarios para las organizaciones más grandes se han omitido por sencillez. Afortunadamente, las similitudes entre la arquitectura y los componentes técnicos empleados en ambas soluciones permite mezclar y ajustar partes de las soluciones con relativa facilidad. La solución *Seguridad en LAN inalámbricas con PEAP y contraseñas* dispone de un apéndice que le ofrece una guía acerca de las partes importantes de cada solución.
  
#### Elección entre WEP dinámica y WPA
  
La protección de datos de WEP, cuando se combina con la autenticación segura y la actualización de clave dinámica proporcionada por 802.1X y EAP, proporciona un nivel de seguridad que es más que adecuado para la mayoría de las organizaciones. No obstante, el estándar WPA mejora por encima de esto y ofrece mejores niveles de seguridad.
  
Las diferencias entre emplear WPA y una WEP dinámica en cualquiera de las soluciones son mínimas y la migración de un entorno WEP dinámico a un entorno WPA es muy sencilla. Los cambios fundamentales al pasar de una WEP dinámica al WPA son:
  
-   Si su hardware de red (puntos de acceso inalámbrico y adaptadores de red inalámbricos) no admite el WPA actualmente, deberá obtener e implementar las actualizaciones de firmware necesarias para ello. Las actualizaciones de firmware para los adaptadores de red inalámbricos se incluyen a menudo en las actualizaciones de controladores de red.
  
-   Deberá activar el WPA en sus puntos de acceso inalámbrico.
  
-   La configuración de cliente WLAN debe modificarse para negociar el WPA en lugar de la seguridad de WEP.
  
-   La directiva de acceso remoto sobre el tiempo de espera de la sesión en el servicio de autenticación de Internet (IAS), que se emplea para imponer una actualización de claves WEP, debería incrementarse con el fin de reducir la carga en el servidor IAS.
  
    **Nota:** IAS es la implementación del servidor RADIUS de Microsoft y se incluye en Windows Server 2003, aunque no se instala de forma predeterminada.
  
WPA debería ser la primera elección, si se encuentra disponible. No obstante, debería reflexionar acerca de si alguno de los siguientes problemas pudiese complicar más el empleo de WPA:
  
-   Es posible que su hardware de red no sea compatible todavía con WPA (es poco probable que ocurra con los nuevos dispositivos, pero es posible que tenga una base amplia de hardware previo a WPA instalada).
  
-   La compatibilidad con la configuración controlada por el GPO sólo se encuentra disponible en el Service Pack 1 de Windows Server 2003 (previsto para la segunda mitad de 2004); las versiones anteriores no eran compatibles así que la configuración de WPA debe establecerse manualmente en los clientes de Windows XP.
  
-   Es posible que WPA no sea compatible con todos sus clientes; por ejemplo, Windows 2000 y anteriores o Pocket PC no disponen en la actualidad de compatibilidad integrada para WPA.
  
Si decide que todavía no se encuentra en condiciones de implementar WPA, debería implementar una solución de WEP dinámica y planear la migración a WPA cuando lo permitan las circunstancias.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Este documento ha intentado proporcionarle la información que necesita para elaborar su estrategia de seguridad para LAN inalámbricas. En la primera parte del documento se han examinado las ventajas empresariales de las redes inalámbricas y también las amenazas de la seguridad para las WLAN escasamente protegidas. En la sección intermedia se ha repasado cómo funciona la seguridad de WLAN basada en 802.1X, EAP y la protección segura de datos para combatir estas amenazas. Las ventajas y desventajas relativas de las distintas opciones tales como VPN, IPSec y seguridad de WEP estática también se han abordado. La sección final incluye orientación sobre qué opciones de seguridad de WLAN seleccionar y cuáles de las soluciones de seguridad de WLAN de Microsoft se ajustaría mejor a su empresa.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Referencias
  
Esta sección ofrece referencias a otra información complementaria importante u otro material informativo de relevancia para este documento.
  
-   La solución de Microsoft para *Seguridad en LAN inalámbricas con PEAP y contraseñas* se encuentra disponible en la siguiente dirección URL:
  
    [http://go.microsoft.com/fwlink/?LinkId=23459](http://go.microsoft.com/fwlink/?linkid=23459)
  
-   La solución de Microsoft para *Solución de Seguridad de LAN inalámbricas — Servicios de Certificate Server de Microsoft Windows Server 2003* se encuentra disponible en la siguiente dirección URL:
  
    [http://go.microsoft.com/fwlink/?LinkId=14843](http://go.microsoft.com/fwlink/?linkid=14843)
  
-   Si precisa información técnica más detallada acerca de IEEE 802.11 y de las tecnologías relacionadas, consulte la sección "802.11 Wireless" del documento de referencia técnica de Windows Server 2003 disponible en la dirección URL:
  
    [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    proddocs/techref/w2k3tr\_wir\_intro.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/proddocs/techref/w2k3tr_wir_intro.mspx)
  
-   Para obtener más información sobre 802.11, consulte la página Web de IEEE 802.11 en:
  
    <http://www.ieee802.org/11/>
  
-   Para obtener más información sobre 802.1X, consulte la página Web de IEEE 802.1X en:
  
    <http://www.ieee802.org/1/pages/802.1x.html>
  
-   Para obtener más información sobre el estándar EAP, consulte RFC 2284 en:
  
    <http://www.ietf.org/rfc/rfc2284.txt?number=2284>
  
-   Para ver una descripción general del estándar WPA de la Alianza Wi-Fi, consulte la siguiente dirección URL:
  
    [http://www.wi-fialliance.org/OpenSection/pdf/  
    Wi-Fi\_Protected\_Access\_Overview.pdf](http://www.wi-fialliance.org/opensection/pdf/wi-fi_protected_access_overview.pdf)
  
-   Para obtener más información sobre las redes inalámbricas, consulte el sitio de redes inalámbricas de Microsoft en la siguiente dirección URL:
  
    <http://www.microsoft.com/wifi>
  
-   Para conocer una descripción detallada de PEAP y cómo se compara con LEAP (además de con EAP-TLS y EAP-MD5), consulte el artículo "The Advantages of Protected Extensible Authentication Protocol (PEAP): A Standard Approach to User Authentication for IEEE 802.11 Wireless Network" en la siguiente dirección URL:
  
    [http://www.microsoft.com/windowsserver2003/techinfo/  
    overview/peap.mspx](http://www.microsoft.com/windowsserver2003/techinfo/overview/peap.mspx)
  
-   El artículo "How Do I Limit My Exposure Against the Wireless LAN Security Threat? The New Realities of Protecting Corporate Information" del grupo META se encuentra disponible en:
  
    [http://www.metagroup.com/cgi-bin/inetcgi/jsp/  
    displayArticle.do?oid=35725](http://www.metagroup.com/cgi-bin/inetcgi/jsp/displayarticle.do?oid=35725)
  
(Este artículo contiene referencias a guías de otros productos y vínculos a sitios Web que sólo están disponibles en inglés.)
  
**Descargue la solución completa en**
  
[Seguridad en LAN inalámbricas con PEAP y contraseñas](http://go.microsoft.com/fwlink/?linkid=23481)
  
[](#mainsection)[Principio de la página](#mainsection)
