---
TOCTitle: 'Apéndice B: Prueba de la Guía de seguridad de Windows XP'
Title: 'Apéndice B: Prueba de la Guía de seguridad de Windows XP'
ms:assetid: '09c716f4-b167-49ec-8122-93e1b8c5f456'
ms:contentKeyID: 20200274
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163067(v=TechNet.10)'
---

Guía de seguridad de Windows XP
===============================

### Apéndice B: Prueba de la Guía de seguridad de Windows XP

Actualizado: 20/10/05

##### En esta página

[](#edaa)[Introducción](#edaa)
[](#ecaa)[Entorno de prueba](#ecaa)
[](#ebaa)[Prueba de la metodología](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Introducción

La función de la *Guía de seguridad deWindows* XP consiste en proporcionar orientaciones probadas y repetibles para la configuración, a fin de proteger los equipos en los que se ejecuta Microsoft® Windows® XP Professional con Service Pack 2 (SP2) en una variedad de entornos.

La *Guía de seguridad* de *Windows* XP se probó en un entorno de laboratorio para garantizar la respuesta esperada. El equipo de pruebas de la *Guía de seguridad* de *Windows *XP comprobó la coherencia de la documentación y todos los procedimientos recomendados en ella. Se realizaron pruebas para comprobar la funcionalidad, pero también para ayudar a los usuarios de la guía a reducir la cantidad de recursos necesarios para crear y probar sus propias implementaciones de la solución.

#### Ámbito

La *Guía de seguridad* de *Windows* XP se probó en condiciones de laboratorio para dos entornos de seguridad diferentes: Cliente de empresa (EC) y Seguridad especializada: Funcionalidad limitada (SSLF). Estos entornos se describen en el capítulo 2, "Configuración de la infraestructura de dominios de Active Directory". Las pruebas se realizaron según los criterios que se describen en la siguiente sección, "Objetivos de la prueba".

No formaba parte de las competencias del equipo de pruebas realizar una evaluación de la vulnerabilidad del entorno del laboratorio de pruebas utilizado para garantizar la seguridad de la solución *Guía de seguridad* de *Windows* XP. Participaron socios, que se encargaron de llevar a cabo pruebas de penetración.

#### Objetivos de la prueba

El equipo de pruebas de la *Guía de seguridad* de *Windows* XP se basó en los siguientes objetivos de prueba:

-   Asegurarse de que la configuración y las opciones de directiva recomendadas para Windows XP Professional con SP2 interoperan correctamente y según lo esperado en una red de dominio basado en Windows Server™ 2003 para los dos entornos de seguridad diferentes.

-   Asegurarse de que los equipos cliente Windows XP Professional SP2 son capaces de llevar a cabo las tareas y las aplicaciones básicas que se enumeran en los casos de prueba incluidos.

-   Comprobar que todas las orientaciones recomendadas en la versión 2.1 de la *Guía de seguridad* de *Windows* XP son claras, completas y técnicamente correctas.

-   Comprobar que las plantillas de seguridad funcionan según lo esperado en el sistema operativo cliente Windows XP Professional SP2.

-   Comprobar que las recomendaciones relativas a las plantillas administrativas y la directiva de restricción de software funcionan según lo esperado en el sistema operativo cliente Windows XP Professional.

Por último, la orientación se debe poder usar de forma repetida y fiable por un ingeniero que tenga la certificación MCSE (Microsoft Certified Systems Engineer) y dos años de experiencia.

[](#mainsection)[Principio de la página](#mainsection)

### Entorno de prueba

El entorno de prueba constaba de un servicio de directorio Windows Server 2003 SP1 Active Directory®, equipos para las funciones de servidor de infraestructura que proporcionaban servicios de controlador de dominio, DNS y DHCP, y otros equipos para funciones de servidor de aplicaciones que proporcionaban servicios de archivos, impresión, entidad emisora de certificados y servicios de correo electrónico con Microsoft Exchange 2003. Los equipos cliente de escritorio y portátiles del dominio utilizaron Windows XP Professional con SP2.

La red contenía también dos equipos cliente que utilizaban Windows XP Professional con SP2 en modo de grupo de trabajo que se emplearon para probar plantillas de seguridad independientes. Los equipos portátiles de la red del dominio se volvieron a utilizar para probar plantillas de seguridad de PC portátiles independientes. En la siguiente figura se ilustra la red de prueba.

[![](images/Cc163067.SGFG0B01(es-es,TechNet.10).jpg)](https://technet.microsoft.com/es-es/cc163067.sgfg0b01_big(es-es,technet.10).jpg)

**Figura B. 1 Red que se utilizó para probar la Guía de seguridad de Windows XP en modo de dominio e independiente**

La red de la figura siguiente se desarrolló para probar las plantillas heredadas que se incluyen con esta guía.

[![](images/Cc163067.SGFG0B02(es-es,TechNet.10).jpg)](https://technet.microsoft.com/es-es/cc163067.sgfg0b02_big(es-es,technet.10).jpg)

**Figura B.2 Red que se utilizó para probar las plantillas de seguridad heredadas que se incluyen con esta guía**

[](#mainsection)[Principio de la página](#mainsection)

### Prueba de la metodología

En esta sección se describen los procedimientos que se siguieron para probar la *Guía de seguridad* de *Windows* XP.

El equipo de pruebas estableció un laboratorio que incorporaba las redes descritas en la sección anterior. Se ejecutó un ciclo rápido de pruebas de modelo (POC) y, después, dos ciclos de pruebas más completos. Durante cada ciclo, el equipo se esforzó por estabilizar la solución.

Se definió un ciclo de pruebas como una secuencia de las dos fases de creación incrementales siguientes:

1.  Fase de configuración manual de los equipos

2.  Fase de configuración de la directiva de grupo/local

En la siguiente sección, "Fases de un ciclo de pruebas", se proporcionan los detalles de cada fase. La sección "Fase de preparación de las pruebas" describe los pasos que se realizaron para garantizar que no había problemas en el laboratorio de pruebas que pudiesen originar una interpretación errónea de los resultados reales de las pruebas después de reforzar la seguridad de los entornos mediante las dos fases de creación incrementales.

En cada ciclo de pruebas, se ejecutaron distintos conjuntos de casos de prueba. Estas pruebas se explican más adelante en este apéndice, en la sección "Tipos de pruebas".

#### Fases de un ciclo de pruebas

Esta solución se probó en las fases que se describen en las subsecciones siguientes. Los problemas graves detectados durante la fase de creación se identificaron como errores y se resolvieron en esa fase antes de que el equipo de pruebas pasase a la siguiente fase incremental. Con este método se aseguraba una resolución rápida de los problemas críticos. También se minimizaba la necesidad de recursos para depurar problemas en fases posteriores.

##### Fase de preparación de las pruebas

En esta fase se configuró la red de línea de base a la que se aplicó la solución. Constó de los pasos que se indican a continuación.

**Para llevar a cabo la fase de preparación de pruebas**

1.  Conecte los equipos en red como se ilustra en el diagrama de red e instale las versiones apropiadas del sistema operativo Windows en todos los equipos servidor y cliente.

2.  Crear y configurar controladores de dominio, dominios y cada función de servidor. Incorporar al dominio los equipos cliente Windows XP Professional con SP2.

3.  Instalar las aplicaciones de usuario en cada uno de los equipos cliente Windows XP Professional con SP2.

4.  Ejecutar las pruebas básicas de comprobación para confirmar que la configuración de red es apropiada. Asegúrese de que el equipo cliente tiene acceso a los servicios proporcionados por el controlador de dominio y los servidores miembro (DNS, DHCP, CA, archivos, impresión, web y correo electrónico).

5.  Ejecutar las aplicaciones instaladas para comprobar que no hay problemas de instalación y que todas las aplicaciones se ejecutan correctamente.

6.  Comprobar el registro de eventos para asegurarse de que no hay errores.

7.  Una vez realizados los pasos anteriores, cree una copia de seguridad de la imagen de cada equipo. Estas imágenes de copia de seguridad se utilizan para revertir las opciones de la red a su estado predeterminado antes de que se inicie un ciclo de pruebas nuevo.

##### Fase de configuración manual

Esta fase es a menudo la primera fase de creación de seguridad. Consta del siguiente procedimiento de generación.

**Para realizar la fase de configuración manual**

1.  El complemento Administración de equipos de Microsoft Management Console (MMC) se utiliza para realizar los cambios de configuración de directiva indicados, como la cuenta y la contraseña del administrador local, en cada equipo miembro. Complete los pasos siguientes para proteger las cuentas de dominio (cuentas Invitado y Administrador):

    1.  Deshabilitar la cuenta de invitado.

    2.  Asegúrese de que la cuenta de Administrador integrada tenga una contraseña compleja, se haya cambiado el nombre y se haya quitado la descripción de cuenta predeterminada.

    3.  Incorpore cualquier recomendación adicional de la guía acerca de cómo garantizar la seguridad de las cuentas de dominio.

2.  Lleve a cabo todos los demás procedimientos de configuración manual de la seguridad según las recomendaciones de los distintos capítulos de la guía.

3.  Para equipos cliente independientes con Windows XP, cree manualmente una base de datos segura.

##### Fase de configuración de Directiva de grupo/local

En esta fase, los objetos de directiva de grupo (GPO) se aplican en los niveles de dominio y unidad organizativa (UO). Los objetos GPO se aplican a las distintas UO con arreglo a las recomendaciones del capítulo 2, "Configuración de la infraestructura de dominios de Active Directory". Para equipos cliente independientes con Windows XP se configura una directiva local. Esta fase consta de los pasos que se indican a continuación.

**Para llevar a cabo la fase de configuración de Directiva de grupo/local**

1.  Cree la estructura de unidades organizativas descrita para seguir las recomendaciones de Directiva de grupo que figuran en la guía.

2.  Mueva los equipos cliente Windows XP de escritorio y portátiles a las UO apropiadas.

3.  Identifique a los usuarios del dominio y muévalos a las UO apropiadas para poder aplicar las plantillas administrativas.

4.  Agregue un nuevo vínculo a GPO para cada UO.

    **Nota**: Quizá deba elevar los vínculos a GPO en la lista de prioridades donde ya hay vínculos a GPO presentes.

5.  Importe en el GPO la plantilla de seguridad incluida con la guía.

6.  Para cada situación del entorno que se ilustra en los distintos capítulos, aplique la directiva de grupo apropiada en cada UO.

#### Detalles de ejecución de las pruebas

En los capítulos 2 a 6 de la *Guía de seguridad* de *Windows* XP se proporcionan instrucciones para aplicar las recomendaciones de la seguridad al dominio, a los equipos Windows XP de escritorio, a los equipos Windows XP portátiles y a los equipos cliente Windows XP independientes en los entornos de Cliente de empresa (EC) y Seguridad especializada: Funcionalidad limitada (SSLF) que se definen en la guía. Estas recomendaciones están acompañadas de un libro de Microsoft Excel®, plantillas de seguridad, Plantillas administrativas y secuencias de comandos automatizadas. Las secuencias de comandos automatizadas se utilizan para importar plantillas en el GPO local en los equipos cliente independientes seguros. En esta sección se explica cómo se implementaron y probaron las recomendaciones.

##### Capítulo 2: Configuración de la infraestructura de dominios de Active Directory

Complete los procedimientos siguientes para probar este capítulo.

**Para comprobar la red de línea de base**

-   Complete los casos de prueba de comprobación básica para asegurarse de que las copias de seguridad de imagen funcionan correctamente. Una ejecución satisfactoria de los casos de prueba confirmará que se cumplen los criterios de entrada.

**Para iniciar la fase de configuración manual**

1.  Sincronice la hora de todos los servidores miembro del dominio y de todos los equipos cliente Windows XP con el controlador de dominio.

2.  Deshabilitar la cuenta de invitado.

3.  Cambie el nombre de las cuentas de Administrador e Invitado.

4.  Cambie la contraseña de Administrador.

**Para implementar la configuración de la estructura de las unidades organizativas**

1.  En el dominio corp.woodgrovebank.com, cree una UO con el nombre "UO Departamento".

2.  Cree dos subunidades organizativas en la UO Departamento. Asígneles los nombres "UO Windows XP" y "UO Usuarios de XP seguros".

3.  En la UO Windows XP, cree las cuatro subunidades organizativas siguientes:

    -   UO Escritorio EC

    -   UO Equipo portátil EC

    -   UO Escritorio SSLF

    -   UO Equipo portátil SSLF

4.  Mueva los equipos Windows XP asignados a cada entorno de seguridad a sus UO respectivas.

5.  Mueva los usuarios del dominio que iniciarán sesión en los equipos cliente Windows XP a la UO Usuarios de XP seguros.

6.  Cree y vincule un GPO nuevo con el nombre "Directiva de dominio" en el objeto corp.woodgrovebank.com. Haga clic en **Subir** en la ficha Directiva de grupo del objeto de dominio en el complemento MMC Usuarios y equipos de Active Directory para asegurar la prioridad más alta para el GPO nuevo, e importe después la plantilla de seguridad adecuada (SSLF-domain.inf o EC-domain.inf) en el GPO.

7.  Ejecute **gpupdate /force** en el controlador de dominio para descargar la última configuración de Directiva de grupo.

##### Capítulo 3: Configuración de seguridad para clientes Windows XP

En este capítulo se describen los parámetros principales que se configuran a través de Directiva de grupo en un dominio Windows Server 2003. En el capítulo se recomiendan configuraciones de directiva para los dos entornos de seguridad definidos a fin de asegurar la protección de los equipos de escritorio y portátiles Windows XP con SP2.

**Para configurar los parámetros de las plantillas de seguridad**

1.  Ejecute las pruebas de implementación de base para comprobar que todas las recomendaciones de la guía resultan apropiadas para su entorno. Revise la configuración de directiva recomendada. Modifique la configuración en las plantillas de seguridad según sea necesario antes de proceder a implementarlas.

2.  Vincule GPO nuevos a cada una de las dos UO Escritorio. Para el entorno de Cliente de empresa, importe la plantilla de seguridad EC-desktop.inf en el GPO. Para el entorno Seguridad especializada: Funcionalidad limitada, importe la plantilla SSLF-desktop.inf en el GPO.

3.  Vincule GPO nuevos a cada una de las dos UO Equipo portátil. Para el entorno de Cliente de empresa, importe la plantilla de seguridad EC-Laptop.inf en el GPO. Para el entorno Seguridad especializada: Funcionalidad limitada, importe la plantilla SSLF-Laptop.inf en el GPO.

4.  Inicie una sesión en un equipo cliente Windows XP y ejecute el **comando gpupdate /force**. A continuación, reinicie el equipo para asegurarse de que se descarga la configuración de Directiva de grupo más reciente.

5.  Ejecute las pruebas que se enumeran más adelante en este documento.

##### Capítulo 4: Plantillas administrativas para Windows XP

En este capítulo se describe cómo configurar y aplicar configuraciones de directiva adicionales en equipos en los que se ejecuta Microsoft Windows XP con SP2 con plantillas administrativas.

**Para configurar los parámetros de las plantillas administrativas**

1.  Ejecute las pruebas de implementación de base para comprobar que todas las recomendaciones de la guía resultan apropiadas para su entorno. Revise la configuración de directiva recomendada. Modifique la configuración en las plantillas administrativas según sea necesario antes de proceder a implementarlas.

2.  Cree cuatro GPO nuevos, uno para cada uno de los cuatro tipos de equipos cliente Windows XP. Dado que existe alguna variación en las configuraciones de directiva para equipos de escritorio y portátiles, se sugiere crear GPO independientes.

    -   Directiva de plantilla administrativa de escritorio en EC

    -   Directiva de plantilla administrativa de portátil en EC

    -   Directiva de plantilla administrativa de escritorio en SSLF

    -   Directiva de plantilla administrativa de portátil en SSLF

3.  En las plantillas administrativas, establezca los parámetros de configuración de equipos y usuarios para cada uno de los GPO según las orientaciones del Capítulo 4, "Plantillas administrativas para Windows XP".

4.  Vincule los GPO a sus UO respectivas.

5.  Inicie una sesión en un equipo cliente Windows XP y ejecute el comando **gpupdate /force**. A continuación, reinicie el equipo para asegurarse de que se descarga la configuración de Directiva de grupo más reciente.

6.  Ejecute las pruebas que se enumeran más adelante en este apéndice.

##### Capítulo 5: Seguridad de clientes Windows XP independientes

En este capítulo se describen las principales configuraciones de directiva que se establecen a través de la directiva del equipo local. Los valores de configuración recomendados ayudarán a proteger los equipos de escritorio y portátiles independientes en la organización en los que se ejecuta Windows XP con SP2.

**Para configurar parámetros de seguridad en clientes Windows XP independientes**

1.  Ejecute las pruebas de implementación de base para confirmar que todas las recomendaciones de la guía resultan apropiadas para su entorno.

2.  Utilice el complemento MMC Configuración y análisis de seguridad para crear una base de datos de seguridad. Esta base de datos se utilizará para escribir la directiva local. En el Capítulo 5, "Seguridad de clientes Windows XP independientes", se proporcionan instrucciones detalladas.

3.  Utilice el complemento Configuración y análisis de seguridad para aplicar las configuraciones de directiva que se incluyen en los archivos de plantillas de seguridad independientes. En el Capítulo 5, "Seguridad de clientes Windows XP independientes", se proporcionan instrucciones paso a paso. Es importante utilizar el complemento Configuración y análisis de seguridad, porque no se pueden aplicar configuraciones de directiva de servicios del sistema con el complemento Directiva de equipo local.

4.  Ejecute la secuencia de comandos automatizada correspondiente (incluida en esta guía) para importar las plantillas de seguridad.

5.  Ejecute las pruebas que se enumeran más adelante en este apéndice.

##### Capítulo 6: Directiva de restricción de software para clientes Windows XP

Este capítulo permite a los administradores identificar y controlar el software que se ejecuta en su dominio. La herramienta que se utiliza es un mecanismo controlado por directivas que recibe el nombre de directiva de restricción de software.

**Para configurar la directiva de restricción de software**

1.  Ejecute las pruebas de implementación de base para confirmar que todas las recomendaciones de la guía resultan apropiadas para su entorno.

2.  Localice la UO que se creó para los equipos Windows XP de escritorio y portátiles. Para equipos cliente independientes, las configuraciones de directiva se ubican en la directiva de seguridad local. Cree un GPO nuevo para la UO Windows XP. Recuerde que este GPO nuevo sólo se utiliza para la directiva de restricción de software.

3.  Configure la directiva de restricción de software de la siguiente manera:

    1.  Cree una directiva de restricción de software predeterminada.

    2.  Configure las reglas de ruta.

    3.  Establezca las opciones de directiva, tales como la aplicación, los tipos de archivo designados y los editores de confianza según las recomendaciones que se proporcionan.

4.  Revise la configuración de directiva y restablezca la opción de directiva predeterminada como **No permitido.**

5.  Inicie una sesión en un equipo cliente Windows XP y ejecute el **comando gpupdate /force**. A continuación, reinicie el equipo para asegurarse de que se descarga la configuración de Directiva de grupo más reciente.

6.  Ejecute las pruebas que se enumeran más adelante en este apéndice.

##### Comprobación de descarga de la directiva de grupo en el cliente XP

En las secciones anteriores se aplicaron los GPO a las UO, que aplicaron los GPO a los equipos en las UO. Realice los pasos siguientes para confirmar la descarga de la directiva de grupo desde el controlador de dominio en un equipo cliente Windows XP. Se supone que el equipo cliente se reinició después de vincular el objeto GPO a la UO.

**Para comprobar la descarga de directiva de grupo en un equipo cliente Windows XP**

1.  Inicie sesión en el equipo cliente Windows XP.

2.  Haga clic en **Inicio** y en **Ejecutar**; escriba **rsop.exe** y presione ENTRAR.

3.  En la consola **Conjunto resultante de directivas**, expanda la **Raíz de consola** y vaya a **Configuración del equipo**.

4.  Haga clic con el botón secundario en **Configuración del equipo** y haga clic en **Propiedades**.

    La lista de GPO se mostrará en el panel **Propiedades de Configuración del equipo**. El GPO aplicado a la UO debe estar disponible en la lista y no debe haber errores asociados al mismo.

5.  Compruebe las configuraciones de directiva de las plantillas administrativas.

    Sólo los parámetros que se configuran en el GPO de plantilla administrativa deben estar visibles en el árbol respectivo de la carpeta **Plantillas administrativas**, bajo **Configuración del equipo** o **Configuración de usuario.**

#### Tipos de pruebas

El equipo de pruebas realizó los siguientes tipos de comprobaciones durante las fases de pruebas para asegurarse de que los equipos cliente Windows XP protegidos sean capaces de realizar las tareas básicas sin una pérdida significativa de funcionalidad. Puede consultar el libro de Excel Windows XP Security Guide Test Cases.xls, que se encuentra en la carpeta **\\Windows XP Security Guide Tools and Templates\\Test Tools** incluida en la descarga de esta guía. Este archivo de libro contiene la lista completa de casos de prueba que se ejecutaron para equipos cliente XP de dominio y equipos cliente XP independientes, así como datos acerca de escenarios de prueba, pasos de ejecución y resultados esperados.

##### Pruebas de aplicaciones

Con estas pruebas se comprueba si funcionan correctamente las aplicaciones de usuario instaladas en los equipos cliente Windows XP (como el conjunto de aplicaciones de Office 2003, Reproductor de Windows Media® y algunas otras). Para obtener información más detallada acerca de los casos de prueba, consulte el libro de Excel Windows XP Security Guide Test Cases.xls que se incluye con esta guía.

##### Pruebas de secuencias de comandos automatizadas

Algunos de los escenarios de casos de prueba se basaron en secuencias de comandos de VBScript. La finalidad principal de estos casos de prueba era comprobar si era correcta la funcionalidad de los equipos cliente con Windows XP que usan servicios basados en red, como inicio de sesión de dominio, cambio de contraseña y acceso al servidor de impresión. Los archivos VBScript para estos casos de prueba están disponibles en la carpeta **\\Windows XP Security Guide Tools and Templates\\Test Tools** que se incluye en la descarga de esta guía.

##### Pruebas básicas de comprobación

Estos casos de prueba son un subconjunto de las pruebas de aplicaciones, de secuencias de comandos automatizadas y de Internet. Son pruebas básicas que cubren una variedad de situaciones diferentes, tales como la capacidad de ejecutar las aplicaciones instaladas en el cliente, la comunicación entre cliente y servidor, la capacidad de tener acceso a Internet y descargar revisiones, y la supervisión de errores en el host. Estos casos de prueba también se ejecutan cuando establece una línea base para la red durante la fase de preparación de pruebas.

##### Pruebas sobre la documentación

Estas pruebas validan que las instrucciones, los procedimientos y las funciones documentadas en la guía de implementación son exactas, no ambiguas y completas. No se incluye una lista de casos de prueba aparte para estas pruebas.

##### Pruebas funcionales

Estas pruebas están diseñadas para comprobar que el sistema que se creó a partir de las instrucciones de generación funciona correctamente y según lo previsto. Con ellas se comprueba la funcionalidad, el estado y el efecto de los procedimientos de generación en los equipos cliente de escritorio y portátiles.

##### Pruebas basadas en Internet

Actualmente, lo normal es que el usuario de cualquier equipo necesite tener acceso a Internet. Con estos casos de prueba se asegura que algunas de las capacidades cotidianas comunes (exploración de sitios Web, uso del servicio Windows Messenger y descarga de actualizaciones críticas del sitio de Microsoft Update) no se vean afectados por el bloqueo del equipo cliente Windows XP.

#### Criterios de corrección y error

Antes de realizar las pruebas, se definieron los siguientes criterios para evitar posibles defectos y garantizar la resolución de errores:

-   Todos los casos de prueba deben pasar el proceso con los resultados esperados, tal como se describe en las hojas de casos de prueba individuales.

-   Se considera que un caso de prueba pasa correctamente el proceso si el resultado real coincide con el resultado esperado que hay documentado para él. Si el resultado real no coincide con el resultado esperado, se considera un caso de prueba con errores y se crea un error, además de asignarse una puntuación de gravedad.

-   Si el caso de prueba tenía errores, no se consideraba que la orientación de la solución fuese necesariamente defectuosa. Por ejemplo, una interpretación errónea de la documentación del producto o una documentación incompleta o no precisa podrían ocasionar errores. Se analizó cada caso para averiguar su causa según los resultados reales y los resultados descritos en la documentación del proyecto. Los errores también se escalaron a los propietarios correspondientes de los productos correspondientes de Microsoft.

#### Criterios para el lanzamiento

El criterio principal para lanzar la *Guía de seguridad* de *Windows* XP estaba relacionado con la gravedad de los errores todavía sin solucionar. Sin embargo, también se trataron otros problemas de los que no se realizaba un seguimiento a través de errores. Los criterios para el lanzamiento son:

-   No hay ningún error sin solucionar con niveles de gravedad 1 y 2.

-   El equipo líder trata todos los errores sin solucionar y se conocen totalmente sus repercusiones.

-   Las guías de la solución no tienen comentarios ni marcas de revisión.

-   La solución pasa satisfactoriamente todos los casos de prueba en el entorno del laboratorio de pruebas.

-   El contenido de la solución no tiene instrucciones conflictivas.

#### Clasificación de los errores

La escala de gravedad de los errores se describe en la tabla siguiente. La escala es de 1 a 4, donde 1 representa la mayor gravedad y 4 la más baja.

**Tabla B.1 Clasificación de la gravedad de los errores**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Gravedad</th>
<th>Tipos más habituales</th>
<th>Condiciones necesarias</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">1</td>
<td style="border:1px solid black;">– El error bloquea la compilación o realización de pruebas adicionales.<br />
– El error causa una accesibilidad del usuario inesperada.<br />
– Los pasos definidos en la documentación no están claros.<br />
– Los resultados o el comportamiento de una función o un proceso contradicen los resultados esperados (según lo documentado en la especificación funcional).<br />
– Existe un error de coincidencia grande entre los archivos de plantillas de seguridad y la especificación funcional.</td>
<td style="border:1px solid black;">– La solución no funciona.<br />
– El usuario no puede empezar a usar partes importantes del sistema.<br />
– El usuario tiene privilegios que no debería tener permitidos.<br />
– Se bloquea el acceso del usuario a determinados servidores en los que se debería permitir.<br />
– No se obtienen los resultados esperados.<br />
– Las pruebas no pueden continuar sin solucionarse.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">2</td>
<td style="border:1px solid black;">– Los pasos definidos en la guía no son claros.<br />
– Falta funcionalidad documentada (en este caso, la prueba se bloquea).<br />
– La documentación falta o no es adecuada.<br />
– Existe una incoherencia entre los archivos de plantillas de seguridad y el contenido de la guía, pero el archivo de plantilla de seguridad está sincronizado con la especificación funcional.</td>
<td style="border:1px solid black;">– El usuario no encuentra una solución sencilla para resolver la situación.<br />
– El usuario no encuentra fácilmente un solución.<br />
– El sistema no cumple los requisitos principales de la empresa.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">3</td>
<td style="border:1px solid black;">– Problema de formato documentado.<br />
– Errores menores de documentación e imprecisiones.<br />
– Faltas de ortografía.</td>
<td style="border:1px solid black;">– El usuario ha encontrado una solución sencilla para resolver la situación.<br />
– El usuario puede solucionar de un modo sencillo la situación.<br />
– El error no produce una mala experiencia para el usuario<br />
.– Los requisitos principales de la empresa siguen siendo funcionales.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">4</td>
<td style="border:1px solid black;">– Sugerencias.<br />
– Mejoras futuras.</td>
<td style="border:1px solid black;">– Claramente no relacionadas con esta versión.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Este documento permite a una organización que implemente la *Guía de seguridad* de *Windows* XP comprender los procedimientos y pasos utilizados para probar la implementación de la solución en un entorno de laboratorio de pruebas. La experiencia real del equipo de pruebas de la *Guía de seguridad* de *Windows* XP se incluye en este documento, que contiene descripciones del entorno de pruebas, los tipos de pruebas, los criterios para el lanzamiento y los detalles de la clasificación de errores.
  
Todos los casos de prueba ejecutados por el equipo de pruebas pasaron el proceso con los resultados esperados. El equipo de pruebas confirmó que la funcionalidad necesaria estaba disponible después de aplicar las recomendaciones de la *Guía de seguridad* de *Windows* XP en los entornos definidos.
  
[](#mainsection)[Principio de la página](#mainsection)
  
##### Download
  
[![](images/Cc163067.icon_exe(es-es,TechNet.10).gif)Descargar la Guía de seguridad de Windows XP](http://go.microsoft.com/fwlink/?linkid=14840)
