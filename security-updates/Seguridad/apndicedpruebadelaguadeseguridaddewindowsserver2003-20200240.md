---
TOCTitle: 'Apéndice D: Prueba de la Guía de seguridad de Windows Server 2003'
Title: 'Apéndice D: Prueba de la Guía de seguridad de Windows Server 2003'
ms:assetid: '6aec7740-ad4a-4bbb-916c-16b8da021179'
ms:contentKeyID: 20200240
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163106(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Apéndice D: Prueba de la Guía de seguridad de Windows Server 2003

##### En esta página

[](#edaa)[Información general](#edaa)
[](#ecaa)[Entorno de prueba](#ecaa)
[](#ebaa)[Prueba de la metodología](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

El objetivo de la *Guía de seguridad de Windows Server 2003* es proporcionar orientación sobre una configuración que se ha probado y usado varias veces para garantizar la seguridad de los equipos que ejecutan Microsoft® Windows* *Server™* *2003 con Service Pack 1 (SP1) en una variedad de entornos.

La *Guía de seguridad de Windows Server 2003* se probó en un entorno de laboratorio para garantizar la respuesta esperada. El equipo de pruebas de la *Guía de seguridad de Windows Server 2003* comprobó la coherencia de la documentación y todos los procedimientos recomendados en ella. Se realizaron pruebas para comprobar la funcionalidad, así como para ayudar a reducir la cantidad de recursos que necesitan los usuarios que utilizan la guía para crear y probar sus propias implementaciones.

#### Ámbito

La *Guía de seguridad de Windows Server 2003* se probó en un laboratorio en el que se simularon tres entornos de seguridad distintos: Cliente heredado (LC), Cliente de empresa (EC) y Seguridad especializada: Funcionalidad limitada (SSLF). Estos entornos se describen en el capítulo 1, "Introducción a la Guía de seguridad de Windows* *Server* *2003". Las pruebas se realizaron en función de los criterios descritos en la sección siguiente, "Objetivos de la prueba".

No formaba parte de las competencias del equipo de pruebas realizar una evaluación de la vulnerabilidad del entorno del laboratorio de pruebas utilizado para garantizar la seguridad de la solución *Guía de seguridad de Windows Server 2003.*

#### Objetivos de la prueba

El equipo de pruebas de la *Guía de seguridad de Windows Server 2003* se basó en los siguientes objetivos de prueba:

-   Validar los cambios recomendados en la configuración de seguridad para los tres niveles de seguridad definidos en la guía. Entre los motivos de estos cambios se incluyen:

    -   Los cambios causados por el lanzamiento del SP1 de *Windows Server 2003*.

    -   El uso de la nueva herramienta Asistente para configuración de seguridad (SCW), disponible en el SP1, y las características nuevas como el Firewall de Windows.

    -   Los comentarios internos y externos recibidos acerca de la versión anterior de la guía.

-   Garantizar que la configuración de seguridad y los cambios de configuración recomendados en la guía cumplen los requisitos de los entornos LC, EC y SSLF.

-   Asegurarse de que los servidores miembro del dominio cuya seguridad se ha reforzado pueden realizar correctamente las tareas de la función asociada.

-   Garantizar que la comunicación entre los equipos cliente y los controladores de dominio no se ve afectada negativamente.

-   Comprobar que todas las orientaciones indicadas son claras, completas y técnicamente correctas.

Por último, la orientación se debe poder usar de forma repetida y fiable por un ingeniero que tenga la certificación MCSE (Microsoft Certified Systems Engineer) y dos años de experiencia.

[](#mainsection)[Principio de la página](#mainsection)

### Entorno de prueba

Las redes del laboratorio de pruebas desarrolladas para probar esta guía fueron similares a las utilizadas en la versión anterior de la guía. Se desarrollaron tres redes diferentes que no obstante eran similares, una para cada uno de los entornos definidos.

Cada red de prueba estaba formada por un bosque de servicio de directorio de Windows* *Server* *2003 con SP1, los equipos para las funciones de servidor de infraestructura que proporcionaban los servicios de controlador de dominio, DNS, WINS y DHCP, y otros equipos para las funciones de servidor de aplicación que proporcionaban los servicios de archivos, impresión y web. La red de EC también incluía equipos para las funciones de Servicios de Certificate Server y servidor IAS; además, en la red de SSLF, se incluyó la función de servidor de host de baluarte (BH). Asimismo, las redes de EC y SSLF incluían Microsoft Operations Manager (MOM) 2005 y Systems Management Server (SMS) 2003 para administrar y supervisar los servidores miembro del dominio y los equipos cliente. Estas redes también incluían Microsoft Exchange* *Server 2003 para el servicio de correo electrónico.

Los equipos cliente de las distintas redes ejecutaban Windows XP Professional con SP2 y Windows 2000 Professional con SP4. La red de LC también incluía equipos cliente que ejecutaban los sistemas operativos Windows 98 SR2 y Windows NT® 4.0 con SP6a.

El siguiente diagrama muestra la red del laboratorio de pruebas desarrollada para el entorno EC.

[![](images/Cc163106.apdxd_fg01(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163106.apdxd_fg01_big(es-es,technet.10).gif)

**Figura D.1 Diagrama lógico de la red del laboratorio de pruebas para el entorno EC**

Para comprobar los escenarios de réplica entre los controladores de dominio cuya seguridad se había reforzado, el bosque de Active Directory constaba de dos sitios. Uno de ellos era el sitio de la oficina principal, con un dominio raíz vacío y un dominio secundario formado por el servidor y los equipos cliente que se han mencionado anteriormente. El segundo sitio constaba simplemente de un segundo controlador de dominio del dominio secundario.

El siguiente diagrama muestra la red del laboratorio de pruebas desarrollada para el entorno SSLF.

[![](images/Cc163106.apdxd_fg02(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163106.apdxd_fg02_big(es-es,technet.10).gif)

**Figura D.2 Diagrama lógico de la red del laboratorio de pruebas para el entorno SSLF**

[](#mainsection)[Principio de la página](#mainsection)

### Prueba de la metodología

En esta sección se describen los procedimientos que se siguieron para probar la *Guía de seguridad de Windows Server 2003*.

El equipo de pruebas estableció un laboratorio que incorporaba las tres redes descritas en la sección anterior. Se ejecutó un ciclo rápido de pruebas de modelo (POC) y, después, dos ciclos de pruebas más completos. Durante cada ciclo, el equipo se esforzó por estabilizar la solución.

Se definió un ciclo de pruebas como una secuencia de las siguientes fases:

1.  Fase de creación de la configuración de seguridad

    -   Fase de configuración manual

    -   Fase de configuración de la directiva de grupo

2.  Fase de ejecución de las pruebas

En la siguiente sección, "Fases de un ciclo de pruebas", se proporcionan los detalles de cada fase. La sección "Fase de preparación de las pruebas" describe los pasos que se realizaron para garantizar que no había problemas en el laboratorio de pruebas que pudiesen originar una interpretación errónea de los resultados reales de las pruebas después de reforzar la seguridad de los tres entornos mediante las dos primeras fases de creación incrementales. También se le conoce como el estado de "línea de base".

#### Fases de un ciclo de pruebas

Las fases del ciclo de pruebas se describen en las subsecciones siguientes. Los problemas graves detectados durante la fase de creación se identificaron como errores y se resolvieron en esa fase antes de que el equipo de pruebas pasase a la siguiente. Este método garantizó la implementación de una configuración de seguridad correcta en la red y validó la precisión de los resultados obtenidos en las pruebas.

##### Fase de preparación de las pruebas

En esta fase se definió la configuración de línea de base que se aplicó a la solución durante la fase de creación de la configuración de seguridad. Para cada uno de los tres entornos, LC, EC y SSLF, se realizaron los siguientes pasos:

**Para realizar la fase de preparación de las pruebas**

1.  Conecte los equipos en red como se ilustra en el diagrama de red e instale las versiones apropiadas del sistema operativo Windows en todos los equipos servidor y cliente.

2.  Cree y configure el dominio, los controladores de dominio y los dos sitios.

3.  Una y configure cada servidor miembro y los servidores de administración. Una también los equipos clientes al dominio.

4.  Ejecute pruebas básicas de comprobación para cada función de servidor con el fin de confirmar si la configuración de la red y de la aplicación es apropiada.

5.  Compruebe el registro de eventos de cada servidor miembro de la red para garantizar que no hay ningún error en el nivel de aplicación o sistema.

6.  Asegúrese de que el equipo cliente tiene acceso a los servicios proporcionados por el controlador de dominio y los servidores miembro (DNS, DHCP, CA, archivos, impresión, web y correo electrónico). Compruebe los registros de eventos de los equipos cliente para asegurarse de que no hay errores.

7.  Asegúrese de que todas las aplicaciones, servicios y agentes necesarios están instalados en cada uno de los miembros del dominio. Por ejemplo, compruebe que el agente MOM está instalado en todos los servidores que administrará el servidor MOM.

8.  Una vez realizados los pasos anteriores, cree una copia de seguridad de la imagen de cada equipo. Estas imágenes de copia de seguridad se utilizan para "revertir" las opciones de la red a la configuración de línea de base antes de que se inicie un ciclo de pruebas nuevo.

##### Fase de creación de la configuración de seguridad

El objetivo de esta fase era seguir los procedimientos de la guía para configurar el dominio, los controladores de dominio y los servidores miembro en un nivel más seguro que el de la configuración de línea de base.

###### Fase de configuración manual

Esta fase es a menudo la primera fase de creación de seguridad. Durante esta fase, se implementaron las recomendaciones de seguridad manuales proporcionadas en cada capítulo.

**Nota**: puede que algunos de estos pasos no sean aplicables a su red. Revise minuciosamente cada procedimiento para conocer la repercusión que puede tener sobre la red.

**Para realizar la fase de configuración manual**

1.  Utilice el complemento Administración de equipos de Microsoft Management Console (MMC) para realizar los cambios de configuración de directiva indicados (como la cuenta y la contraseña del administrador local) en cada equipo miembro. Siga los pasos siguientes para garantizar la seguridad de las cuentas de dominio:

    1.  Asegúrese de que la cuenta de administrador local tiene una contraseña difícil, que se ha cambiado su nombre y que se le ha quitado la descripción de cuenta predeterminada.

    2.  Cambie el nombre de las cuentas de invitados en el host y deshabilítelas.

    3.  Incorpore cualquier recomendación adicional de la guía acerca de cómo garantizar la seguridad de las cuentas de dominio.

2.  Agregue cualquier grupo o cuenta de seguridad a la configuración de derechos de usuarios, tal como se describe en los capítulos.

3.  Realice el resto de procedimientos manuales de seguridad aplicables, tal como se indica en cada capítulo. Por ejemplo, habilite la opciones de configuración de volcados manuales de memoria y de informe de errores.

###### Fase de configuración de la directiva de grupo

El propósito de esta fase es crear y aplicar los objetos de directiva de grupo (GPO) a los niveles de dominio y unidad organizativa (UO). Los GPO se aplican a las distintas UO según las recomendaciones que se incluyen en el capítulo 2, "Mecanismos de seguridad de Windows* *Server* *2003".

El Service Pack 1 de Windows Server 2003 incluye algunas herramientas y características nuevas que suponen un cambio en el diseño de la implementación de la directiva de grupo con respecto a la versión anterior.

SCW es una herramienta de reducción de la superficie de ataque que sirve para crear el conjunto necesario de directivas de seguridad para cada una de las funciones de servidor que se describen en esta guía. La disponibilidad de SCW causó dos cambios importantes en la fase de configuración de la directiva de grupo:

-   Los filtros IPSec proporcionados con la versión anterior de esta guía se reemplazaron por configuraciones de puerto del Firewall de Windows creadas con SCW.

-   Las plantillas de seguridad incluidas con la guía se deben utilizar junto con SCW para crear archivos de plantillas de seguridad XML. Estas plantillas se convierten después en los GPO correspondientes mediante la herramienta de línea de comandos Scwcmd.

Se repitieron los pasos siguientes para cada uno de los tres entornos de seguridad:

**Para crear objetos de directiva de grupo**

1.  Asegúrese de que todas las aplicaciones, servicios y agentes necesarios están instalados en cada uno de los miembros del dominio de la red de línea de base. Por ejemplo, compruebe que el agente MOM está instalado en todos los servidores miembro del dominio que administrará MOM.

2.  Utilice el complemento MMC Usuarios y equipos de Active* *Directory para crear la estructura de UO descrita.

3.  Cree el GPO de directiva de dominio con la plantilla de seguridad .inf. Para este paso no es necesario utilizar SCW.

4.  Utilice la herramienta SCW para crear plantillas de seguridad basadas en XML para cada función de servidor descrita en la guía. Los pasos preceptivos se describen en el capítulo 2, "Mecanismos de seguridad de Windows* *Server* *2003", y en los capítulos de cada función de servidor. Cuando realice este paso, incluya la plantilla de seguridad .inf apropiada para la función del servidor. Los archivos de plantilla se incluyen con la versión descargable de esta guía.

5.  Utilice la herramienta de línea de comandos Scwcmd para convertir las plantillas de seguridad XML creadas en el paso anterior en objetos GPO.

6.  Repita el paso 4 en el servidor host de baluarte para crear la plantilla de seguridad XML del host de baluarte y, a continuación, vuelva a utilizar SCW para convertirla y aplicarla al GPO local.

Una vez creados correctamente los GPO, compare la configuración con la información de los capítulos para identificar si hay alguna configuración incorrecta.

En esta fase, todos los servidores miembro del dominio residen en la UO Equipos. Estos servidores se mueven después a las UO correspondientes de la UO Servidor miembro.

La siguiente tarea (detallada en el siguiente procedimiento) consiste en aplicar cada uno de estos GPO a las UO correspondientes. Se utilizó la herramienta Consola de administración de directivas de grupo (GPMC) para vincular el GPO a la UO. Por último, se vinculó el GPO de directiva de controladores de dominio.

Se realizaron los pasos siguientes para llevar a cabo el resto de la fase de creación de la configuración de seguridad:

**Para aplicar objetos de directiva de grupo**

1.  Vincule el GPO de directiva de grupo al objeto de dominio.

    **Nota**: si los vínculos de GPO predeterminados ya existen o hay varios GPO, puede que tenga que elevar los vínculos de GPO en la lista de prioridades.

2.  Utilice la herramienta Consola de administración de directivas de grupo para vincular el GPO Directiva de línea de base de servidores miembro a la UO Servidores miembro. (También puede realizar este paso con el complemento MMC Usuarios y equipos de Active* *Directory.)

3.  Vincule cada GPO de función de servidor individual a la UO de función de servidor apropiada.

4.  Vincule el GPO Directiva de controlador de dominio a la UO Controlador de dominio.

5.  Para asegurarse de que se aplica la configuración de directiva de grupo más reciente, ejecute **gpudpate /force** en una ventana del símbolo del sistema en todos los controladores de dominio. A continuación, reinicie todos los controladores de dominio, uno por uno, empezando por el controlador de dominio principal. Deje transcurrir un tiempo suficiente para que Active* *Directory replique los cambios entre los sitios.

    **Importante**: es muy importante reiniciar los controladores de dominio después de aplicar el GPO Directiva de controladores de dominio. Si no realiza este paso, tal vez vea errores en la carpeta del servicio de directorio o errores Userenv en la carpeta Aplicación del Visor de eventos.

6.  Repita el paso 5 en todos los servidores miembro del dominio.

7.  Compruebe si hay errores en el Visor de eventos. Revise los registros de errores para solucionar problemas y resolver cualquier error.

8.  En el servidor host de baluarte, utilice la herramienta SCW para aplicar la plantilla de seguridad XML de host de baluarte en el GPO local del servidor.

###### Comprobación de la descarga de la directiva de grupo en los equipos servidor miembro

Con los procedimientos anteriores se crearon los GPO y se aplicaron a las UO para configurar los equipos de esas UO. Siga los pasos siguientes para confirmar que se ha descargado correctamente la directiva de grupo de los controladores de dominio en los equipos servidor miembro. (Se asume que los equipos servidor miembro se reiniciaron después de vincular el GPO a la UO.)

**Para comprobar la descarga de la directiva de grupo en un equipo servidor miembro**

1.  Inicie sesión en el equipo servidor miembro.

2.  Haga clic en **Inicio** y en **Ejecutar**; escriba **rsop.exe** y presione ENTRAR.

3.  En la consola **Conjunto resultante de directivas**, expanda la **Raíz de consola** y vaya a **Configuración del equipo**.

4.  Haga clic con el botón secundario en **Configuración del equipo** y haga clic en **Propiedades.**

    La lista de GPO se mostrará en el panel **Propiedades de Configuración del equipo**. El GPO aplicado a la UO debe estar disponible en la lista y no debe haber errores asociados al mismo.

##### Fase de ejecución de las pruebas

Esta fase ejecuta los casos de prueba desarrollados por el equipo de pruebas. El objetivo de la fase de ejecución de las pruebas es identificar lo siguiente:

-   Cualquier evento potencial de aplicación, seguridad o error del sistema originado por los procesos utilizados para reforzar la seguridad del dominio, los controladores de dominio, los servidores miembro o el servidor host de baluarte.

-   La pérdida de disponibilidad de un servicio o funcionalidad debido a cambios en la configuración de seguridad de los servidores de la red.

-   Imprecisiones técnicas entre lo que se indica en los capítulos y la implementación física en el laboratorio de pruebas.

El equipo de pruebas ejecutó el conjunto de casos de prueba que se incluyen en la carpeta \\**Windows Server 2003 Security Guide Tools and Templates\\Test Tools**. (En la versión descargable de esta guía se incluyen las herramientas y plantillas.) Estas pruebas se ejecutaron en cada una de las tres redes, excepto en aquellas en las que se probaron componentes que sólo estaban disponibles en una red, como Servicios de Certificate Server, que sólo estaba disponible en el entorno EC. Además de estos casos de prueba, se realizaron pruebas manuales en determinados momentos; por ejemplo, para comprobar periódicamente los registros del Visor de eventos o cualquier problema específico descubierto en la versión anterior de la guía. Todos los problemas encontrados se registraron en una base de datos y los miembros del equipo de desarrollo los probaron hasta resolverlos.

En la siguiente sección se proporciona información más detallada acerca de los distintos tipos de pruebas realizados.

#### Tipos de pruebas

El equipo de pruebas realizó los siguientes tipos de pruebas durante las fases de prueba para garantizar que el dominio, los controladores de dominio y los servidores miembro protegidos no tenían ninguna pérdida de funcionalidad. Es posible que desee consultar los libros de Excel, disponibles en la carpeta **\\Windows Server 2003 Security Guide Tools and Templates\\Test Tools**, que se incluyen en la versión descargable de esta guía. Estos libros contienen la lista completa de casos de prueba ejecutados para los servidores basados en dominio y los servidores independientes que ejecutan Windows Server 2003 con SP1. También se proporcionan detalles tales como escenarios de prueba, pasos de ejecución y resultados esperados.

Estas pruebas se ejecutaron varias veces. Y, lo que es más importante, se ejecutaron antes y después de implementar la configuración de seguridad que se describe en esta guía. Este enfoque ayudó al equipo de pruebas a identificar errores potenciales y cualquier variación de funcionalidad en las funciones de servidor indicadas.

##### Pruebas en el lado cliente

Estos casos de prueba se ejecutaron en los equipos cliente de la red. El propósito principal de estas pruebas era garantizar que los servicios del dominio (como autenticación, derechos de acceso, resolución de nombres, etc.) y los servicios basados en aplicación (como de archivos, impresión y web) estaban disponibles en los equipos cliente después de reforzar la seguridad de los servidores de la red. Para el entorno LC, estas pruebas garantizaron que los equipos cliente que ejecutaban el SP6a de Windows* *NT* *4.0 y Windows* *98 podían autenticarse con el dominio de Active* *Directory de Windows* *Server* *2003.

##### Pruebas sobre la documentación

Estas pruebas validan que las instrucciones, los procedimientos y las funciones documentadas en la guía de implementación son exactas, no ambiguas y completas. No se incluye una lista de casos de prueba aparte para estas pruebas.

##### Pruebas de secuencias de comandos

Algunos de los escenarios de prueba de los clientes se basaron en secuencias de comandos de VBScript. La finalidad principal de estos casos de prueba era comprobar si era correcta la funcionalidad de los equipos cliente con Windows XP que usan servicios basados en red, como inicio de sesión de dominio, cambio de contraseña y acceso al servidor de impresión. Los archivos VBScript de estos casos de prueba están disponibles en la carpeta **\\Windows Server 2003 Security Guide Tools and Templates\\Test Tools** de la versión descargable de esta guía.

##### Pruebas en el servidor

Estos casos de prueba se realizaron para comprobar la funcionalidad y la repercusión de los procedimientos de compilación de los servidores con el SP1 de Windows* *Server* *2003 que se protegieron según las recomendaciones de esta guía. Se probaron todas las funciones de servidor descritas en esta guía. También se probaron funciones de servidor adicionales incluidas en la red de prueba, como Exchange, MOM y SMS.

#### Criterios de corrección y error

Antes de realizar las pruebas, se definieron los siguientes criterios para evitar posibles defectos y garantizar la resolución de errores:

-   Todos los casos de prueba deben pasar el proceso con los resultados esperados, tal como se describe en las hojas de casos de prueba individuales.

-   Se considera que un caso de prueba pasa correctamente el proceso si el resultado real coincide con el resultado esperado que hay documentado para él. Si el resultado real no coincide con el resultado esperado, se considera un caso de prueba con errores y se crea un error, además de asignarse una puntuación de gravedad.

-   Si el caso de prueba tenía errores, no se consideraba que la orientación de la solución fuese necesariamente defectuosa. Por ejemplo, una interpretación errónea de la documentación del producto o una documentación incompleta o no precisa podrían ocasionar errores. Se analizó cada caso para averiguar su causa según los resultados reales y los resultados descritos en la documentación del proyecto. Los errores también se escalaron a los propietarios correspondientes de los productos correspondientes de Microsoft.

#### Criterios para el lanzamiento

El criterio principal para lanzar la *Guía de seguridad de Windows Server 2003* estaba relacionado con la gravedad de los errores todavía sin solucionar. Sin embargo, también se trataron otros problemas de los que no se realizaba un seguimiento a través de errores. Los criterios para el lanzamiento son:

-   No hay ningún error sin solucionar con niveles de gravedad 1 y 2.

-   El equipo líder trata todos los errores sin solucionar y se conocen totalmente sus repercusiones.

-   Las guías de la solución no tienen comentarios ni marcas de revisión.

-   La solución pasa satisfactoriamente todos los casos de prueba en el entorno del laboratorio de pruebas.

-   El contenido de la solución no tiene instrucciones conflictivas.

#### Clasificación de los errores

La escala de gravedad de los errores se describe en la tabla siguiente. La escala es de 1 a 4, donde 1 representa la mayor gravedad y 4 la más baja.

**Tabla D.1: Clasificación de la gravedad de los errores**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Gravedad</p></th>
<th><p>Tipos más habituales</p></th>
<th><p>Condiciones necesarias</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>– El error bloquea la compilación o realización de pruebas adicionales.<br />
– El error causa una accesibilidad del usuario inesperada.<br />  
– Los pasos definidos en la documentación no están claros.<br />  
– Los resultados o el comportamiento de una función o un proceso contradicen los resultados esperados (según lo documentado en la especificación funcional).<br />
– Existe un error de coincidencia grande entre los archivos de plantillas de seguridad y la especificación funcional.</p></td>
<td style="border:1px solid black;"><p>– La solución no funciona.<br />
– El usuario no puede empezar a usar partes importantes del equipo o la red.<br />  
– El usuario tiene privilegios que no debería tener permitidos.<br />  
– Se bloquea el acceso del usuario a determinados servidores en los que se debería permitir.<br />  
– No se obtienen los resultados esperados.<br />
– Las pruebas no pueden continuar sin solucionarse.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>2</p></td>
<td style="border:1px solid black;"><p>– Los pasos definidos en la guía no son claros.<br />
– Falta funcionalidad documentada (en este caso, la prueba se bloquea).<br />  
– La documentación falta o no es adecuada.<br />
– Existe una incoherencia entre los archivos de plantillas de seguridad y el contenido de la guía, pero el archivo de plantilla de seguridad está sincronizado con la especificación funcional.</p></td>
<td style="border:1px solid black;"><p>– El usuario no encuentra una solución sencilla para resolver la situación.<br />
– El usuario no encuentra fácilmente un solución.<br />
– El equipo o la red no pueden cumplir los requisitos principales de la empresa.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>3</p></td>
<td style="border:1px solid black;"><p>– Problema de formato documentado.<br />
– Errores menores de documentación e imprecisiones.<br />
– Faltas de ortografía.</p></td>
<td style="border:1px solid black;"><p>– El usuario ha encontrado una solución sencilla para resolver la situación.<br />
– El usuario puede solucionar de un modo sencillo la situación.<br />  
– El error no produce una mala experiencia para el usuario.<br />
– Los requisitos principales de la empresa siguen siendo funcionales.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>4</p></td>
<td style="border:1px solid black;"><p>– Sugerencias.<br />
– Mejoras futuras.</p></td>
<td style="border:1px solid black;"><p>– Claramente no relacionadas con esta versión.</p></td>
</tr>  
</tbody>  
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Este apéndice permite a una organización que utilice la *Guía de seguridad de Windows Server 2003* comprender los procedimientos y pasos utilizados para probar la implementación de la solución en un entorno de laboratorio de pruebas. La experiencia real del equipo de pruebas de la *Guía de seguridad de Windows Server 2003* se incluye en este apéndice, que contiene descripciones del entorno de pruebas, los tipos de pruebas, los criterios para el lanzamiento y los detalles de la clasificación de errores.
  
Todos los casos de prueba ejecutados por el equipo de pruebas pasaron el proceso con los resultados esperados. El equipo de pruebas confirmó que la funcionalidad necesaria estaba disponible después de aplicar las recomendaciones de la *Guía de seguridad de Windows Server 2003* en los entornos definidos.
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)
  
[](#mainsection)[Principio de la página](#mainsection)
