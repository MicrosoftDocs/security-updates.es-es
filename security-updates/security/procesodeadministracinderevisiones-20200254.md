---
TOCTitle: Proceso de administración de revisiones
Title: Proceso de administración de revisiones
ms:assetid: '1da5ae9e-dbb1-4960-b90d-8669bf8397cb'
ms:contentKeyID: 20200254
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc700830(v=TechNet.10)'
---

Proceso de administración de revisiones
=======================================

### Fase 1: Valoración

Actualizado: junio 1, 2007

##### En esta página

[Descripción del módulo](#eye)

[Objetivos](#eaf)

[Aplicable a](#ech)

[Uso del módulo](#enaac)

[Información general](#excac)

[Inventario de activos informáticos existentes](#ekfac)

[Valorar las amenazas y vulnerabilidades de seguridad](#ekfbc)

[Determinar la mejor fuente de información acerca de las actualizaciones de software](#ekfcc)

[Valorar la infraestructura de distribución de software existente](#ekfdc)

[Valorar la eficacia operativa](#ekfec)

[Resumen](#ekffc)

[Paso a la fase de identificación](#ekfgc)

Descripción del módulo
----------------------

En este módulo se describe la primera fase, Valoración, del proceso de administración de actualizaciones de cuatro fases. La fase de valoración está relacionada con la auditoría de software en su entorno de producción, la evaluación de las amenazas y vulnerabilidades de seguridad potenciales y la valoración de la infraestructura de administración de actualizaciones.

El objetivo de este módulo es describir los principios de la fase de valoración del proceso de administración de actualizaciones, así como ofrecer una introducción a los tipos de tareas que le permitirán llevar a cabo la valoración mediante Microsoft Windows Server Update Services (WSUS) y Microsoft Systems Management Server (SMS).

**Nota:** la versión beta 2 del próximo lanzamiento de SMS, denominada System Center Configuration Manager 2007, está disponible para su descarga en [http://www.microsoft.com/technet/sms/2007/evaluate/download.mspx](http://www.microsoft.com/technet/solutionaccelerators/msf/default.mspx). Con excelentes mejoras en simplicidad, configuración, implementación y seguridad, Configuration Manager 2007 simplifica en gran medida la implementación del sistema, la automatización de tareas, la administración del cumplimiento de normativas así como la administración de la seguridad basada en directivas, lo cual permite la mejora de la agilidad empresarial.

Después de leer este módulo podrá planear las tareas que necesita determinar:

-   Elementos de su entorno de producción.
-   Amenazas y vulnerabilidades de seguridad que puede afrontar.
-   Cómo y cuándo estará preparada su organización para responder a nuevas actualizaciones de software.

Sin un proceso de valoración continua, no podrá saber qué activos informáticos tiene, cómo los puede proteger y cómo se puede asegurar de que su arquitectura de distribución de software es compatible con la administración de actualizaciones.

[](#mainsection)[Principio de la página](#mainsection)

Objetivos
---------

Use este módulo para:

-   Inventario de activos informáticos existentes.
-   La valoración de las vulnerabilidades y amenazas de seguridad.
-   Determinar la mejor fuente de información acerca de nuevas actualizaciones de software.
-   La valoración de la infraestructura de distribución de software existente.
-   La valoración de la efectividad operativa.

[](#mainsection)[Principio de la página](#mainsection)

Aplicable a
-----------

Este módulo se aplica a los siguientes productos y tecnologías:

-   Todos los productos y tecnologías de Microsoft

[](#mainsection)[Principio de la página](#mainsection)

Uso del módulo
--------------

En este módulo se describe la fase de valoración del proceso de administración de actualizaciones de cuatro fases. Se describen las tareas básicas necesarias para llevar a cabo la valoración mediante Microsoft Windows Server Update Services (WSUS) y Microsoft Systems Management Server (SMS).

Para obtener el máximo rendimiento del módulo:

-   Lea el capítulo Introducción del módulo "Proceso de administración de actualizaciones". En este capítulo se ofrece información general de todas las fases del proceso de administración de actualizaciones de cuatro fases y se proporciona una introducción a las herramientas disponibles para aplicar la administración de actualizaciones en los entornos del sistema operativo Microsoft Windows.
-   Use las bibliotecas técnicas de WSUS y SMS para obtener materiales de referencia más detallados. Estas bibliotecas se encuentran en:
    -   [Biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true)
    -   [Biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx)

[](#mainsection)[Principio de la página](#mainsection)

Información general
-------------------

La fase de valoración es la primera fase principal del proceso de administración de revisiones que se muestra en la figura 1.

![](images/Cc700830.secmod194figure1(es-es,TechNet.10).gif)
**Figura 1 El proceso de administración de revisiones**

Idealmente, es un proceso continuo que debe seguir para asegurarse de que siempre conoce los activos informáticos que posee, cómo los puede proteger y cómo puede asegurarse de que su arquitectura de distribución de software es compatible con la administración de actualizaciones.

El resto de esta sección se centrará en los requisitos clave de la valoración continua. Los requisitos son:

-   Inventario de activos informáticos existentes.
-   La valoración de las vulnerabilidades y amenazas de seguridad.
-   Determinar la mejor fuente de información acerca de nuevas actualizaciones de software.
-   La valoración de la infraestructura de distribución de software existente.
-   La valoración de la efectividad operativa.

[](#mainsection)[Principio de la página](#mainsection)

Inventario de activos informáticos existentes
---------------------------------------------

Desde la perspectiva de la automatización de la administración de actualizaciones, hay dos tipos de objetivos de inventario. Los sistemas que se administran, mediante una herramienta de administración como Microsoft Windows Server Update Services (WSUS) o Systems Management Server (SMS), se clasifican como infraestructura administrada. Los que no tienen un agente SMS funcional, un cliente de Actualizaciones automáticas funcional (para usar con WSUS), o que a propósito se han excluido de la automatización de administración, se consideran infraestructura no administrada. La infraestructura no administrada puede incluir sistemas tales como:

-   Sistemas de seguridad, hosts externos y DMZ, y sistemas conocidos en entornos específicos como prueba y desarrollo.
-   Equipos independientes.

Los activos no administrados todavía necesitan tratamiento por parte de la administración de actualizaciones. Debe comprobar estos sistemas para asegurarse de que se han instalado las actualizaciones de software más recientes. Las revisiones manuales, o el uso de Microsoft Update, podrían ser la forma más efectiva de implementar actualizaciones de software en tales sistemas.

La identificación de los requisitos de administración de actualizaciones de equipos independientes o de equipos que no son miembros de un dominio bajo su control puede suponer un desafío. Sin derechos administrativos locales para estos clientes no administrados, puede resultar difícil recopilar información del sistema que vaya más allá del nombre del equipo y la dirección del Protocolo de Internet (IP). Sin embargo, esta información básica puede servir como base para identificar clientes no administrados en su entorno.

**Nota:** Para sistemas basados en Microsoft Windows, Microsoft Baseline Security Analyzer (MBSA) notificará los nombres y direcciones IP del equipo que no puede examinar debido a que la cuenta de usuario que inicia el examen no tiene derechos administrativos para los equipos de destino.

### ¿Qué información se debe recopilar?

La administración efectiva de actualizaciones requiere un conocimiento exacto y actualizado acerca del hardware y el software que se han implementado en el entorno de producción. Sin esta información, no podrá determinar los equipos de su entorno que requieren una actualización de software. También es importante determinar la forma en que los equipos cliente están conectados a la red. Si algún equipo se conecta a través de vínculos lentos o no confiables, o bien usa acceso remoto, como acceso telefónico, el método de distribución e instalación de una actualización de software será diferente al método que se usa para los equipos que están conectados a una red rápida y confiable.

En las siguientes secciones se describe la información que se debe recuperar de los equipos implementados en el entorno de producción para realizar una administración efectiva de actualizaciones.

#### Identificar las versiones y tipos de hardware

Comprender si un equipo es portátil (cliente móvil), de escritorio o servidor ayudará a los administradores a determinar cómo se debe instalar una actualización de software determinada. Por ejemplo, si actualiza un servidor, puede que necesite observar intervalos de interrupción (momentos específicos en los cuales se permiten cambios y reinicios de equipo) o asegurarse de hacer copias de seguridad del servidor antes de implementar la actualización de software.

SMS permite crear colecciones que incluyen servidores que se pueden actualizar en un período de interrupción específico, lo cual garantiza que las actualizaciones de software no se instalan durante las operaciones empresariales normales. Para obtener más información acerca del uso de SMS en la fase de valoración, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

#### Identificar los tipos y versiones del sistema operativo

Los administradores deben conocer todos los tipos y versiones de sistema operativo (SO) que se hayan implementado en el entorno de producción. MBSA notificará acerca de cualquier actualización de seguridad o Service Pack que falten e identificará vulnerabilidades para las instalaciones de los sistemas operativos Microsoft Windows Server™ 2003, Windows Vista, Windows XP, Windows 2000 y Windows NT 4.0. También notificará si la configuración del equipo cumple con las recomendaciones de seguridad habituales (tales como contraseñas seguras).

#### Identificar aplicaciones y software intermedio

Al igual que sucede con la versión de Service Pack y del sistema operativo, los administradores deben conocer todas las versiones y aplicaciones de software implementadas.

Si implementa WSUS, debe usar MBSA 2.0.1 para identificar actualizaciones de software que faltan. MBSA también identificará los parámetros de seguridad mal configurados para ciertas aplicaciones (por ejemplo Microsoft Office, Internet Information Server (IIS), Internet Explorer y Microsoft SQL Server™). Para obtener más información acerca del uso de WSUS en la fase de valoración, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true).

Si usa SMS 2003, el Agente cliente de inventario de hardware se puede usar para recopilar información acerca de todas las aplicaciones instaladas, Service Packs y actualizaciones de software que se han registrado en el programa Agregar o quitar programas de Windows. El Agente cliente de inventario de hardware de SMS 2003 se puede usar para obtener detalles de cada archivo ejecutable (.exe) instalado, entre los que se incluyen todas las aplicaciones, incluso las que no se registren en Agregar o quitar programas. Para obtener más información acerca del uso de SMS en la fase de valoración, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

#### Determinar funciones

Es esencial determinar la función de un equipo debido a que los administradores necesitan esta información para evaluar las consecuencias de reiniciar el equipo una vez que se haya implementado la actualización de software. Por ejemplo:

-   Si el equipo es un servidor que ejecuta una aplicación crítica para la empresa, puede que tenga que volver a programar la instalación de la actualización de software para períodos en los cuales ésta tendrá el menor impacto en la empresa. También puede que sea necesario tomar medidas para mantener la continuidad empresarial; por ejemplo, que los usuarios puedan seguir con el uso de la aplicación mientras se reinicia el servidor.
-   Si el equipo es un controlador de dominio que almacena una o varias funciones de maestro de operaciones también denominadas operaciones de maestro único flexible (FSMO), debe desplazar estas funciones a otros controladores de dominio en el dominio mientras se actualiza el equipo. Debe restaurar las funciones en el equipo original cuando éste se reinicie correctamente.

Si usa SMS 2003, el Agente cliente de inventario de hardware puede notificar de los servicios que se ejecutan en un equipo determinado. Para obtener más información acerca del uso de SMS en la fase de valoración, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

Nota: Tal como se mencionó anteriormente en el Módulo de introducción, la versión beta 2 del próximo lanzamiento de SMS, denominada System Center Configuration Manager 2007, está disponible para su descarga en [http://www.microsoft.com/technet/sms/2007/evaluate/download.mspx](http://www.microsoft.com/technet/solutionaccelerators/msf/default.mspx).

#### Descripción de la conectividad

Comprender el esquema de la infraestructura de red, sus capacidades, nivel de seguridad, velocidad de vínculo y disponibilidad de vínculo es importante para realizar actualizaciones efectivas. Las actualizaciones de software pueden variar en tamaño y conocer las limitaciones de la infraestructura de su red puede reducir potencialmente cualquier retraso en la distribución de actualizaciones de software. También puede determinar la forma en la que se implementará la actualización de software en determinados equipos cliente.

La detección de redes de SMS puede proporcionar información acerca de la topología de red y los dispositivos conectados a la red. Para obtener más información acerca del uso de SMS en la fase de valoración, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

#### Identificar las actualizaciones de software instaladas y las que faltan

Es fundamental la identificación de las actualizaciones de software que se han instalado en el equipo. Si usa WSUS, debe emplear MBSA para determinar las actualizaciones de software que son necesarias en los servidores y estaciones de trabajo de su organización, debido a que WSUS no incluye herramientas de auditoría específicas. Sin embargo, MBSA no puede detectar la presencia o ausencia de actualizaciones de software para todos los sistemas operativos y aplicaciones de software. Para obtener una lista completa de las actualizaciones de software que puede detectar, consulte el artículo 895660 de Microsoft Knowledge Base acerca de la disponibilidad de Microsoft Baseline Security Analyzer (MBSA) 2.0 en [http://support.microsoft.com/kb/895660](http://www.microsoft.com/technet/solutionaccelerators/msf/default.mspx). Si su organización requiere una auditoría integral de hardware y software, la capacidad de actualizar aplicaciones instaladas, como SQL Server 2000, y la capacidad de implementar actualizaciones de software que no estén relacionadas con la seguridad, debe considerar la posibilidad de implementar SMS para que sea compatible con la administración de actualizaciones. Para obtener más información acerca del uso de WSUS en la fase de valoración, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true).

Si usa SMS 2003, puede emplear las herramientas Security Updates Inventory Tool e Inventory Tool for Microsoft Updates (parte de la Administración de las actualizaciones de software) para ampliar el inventario de hardware de SMS con el fin de que notifique las actualizaciones de software que se deben instalar en un conjunto de clientes. Los clientes de SMS 2003 comparan lo que se ha instalado según la lista de actualizaciones de software disponible que se incluye en el último catálogo de actualizaciones de software (Mssecure.cab) descargado del sitio web de Microsoft Update. Aunque esta herramienta no notificará los Service Pack que faltan, puede usar los agentes cliente de inventario de hardware y software SMS para averiguar el Service Pack instalado actualmente. SMS 2003 también incluye Microsoft Office Inventory Tool for Updates, parte de la Administración de actualizaciones de software. Amplía el inventario de hardware de SMS de forma que notifique de actualizaciones de software requeridas de Microsoft Office. Para obtener más información acerca del uso de SMS en la fase de valoración, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

### Inventario y auditoría

Una auditoría ayuda a que una organización comprenda y obtenga registros exactos de su entorno de producción antes de determinar las líneas de base mediante las herramientas identificadas anteriormente. También debe agregar los resultados de la auditoría hasta este punto al repositorio central de su organización para efectuar el seguimiento de la información acerca del entorno de producción. Actuará de punto de referencia doble, lo que garantiza que la auditoría no sólo es correcta, sino que también cuenta con un repositorio actualizado. Se deben observar las diferencias entre el resultado de auditoría y el registro del repositorio y transmitir esa información a su equipo de administración de problemas para que la investigue. Los miembros del equipo de administración de problemas deben intentar determinar el punto de error en el registro de la información e implementar una solución si es necesario, para evitar casos similares en el futuro.

Debido a que contar con información exacta y actualizada acerca de lo que hay en el entorno es fundamental para la administración de actualizaciones, los administradores deben comprobar que se ha llevado a cabo una auditoría antes de comenzar a usar WSUS o SMS para implementar actualizaciones de software en el entorno de producción.

Si usa WSUS, necesitará MBSA para identificar las aplicaciones instaladas, así como las actualizaciones que faltan para que esas aplicaciones sean seguras. Para obtener más información acerca del uso de WSUS en la fase de valoración, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true).

Si usa SMS 2003, el primer paso para comprobar si las auditorías son correctas es confirmar que las herramientas Microsoft Office Inventory Tool for Updates y Security Updates Inventory Tool se hayan ejecutado correctamente. Para ello, se consultan los mensajes de estado para comprobar si ha habido errores. Luego, debe comprobar el estado del inventario de hardware y software en cada cliente SMS mediante la creación de un informe web que enumere los equipos cliente de SMS en los que los agentes cliente de inventario de hardware y software no han podido realizar la instalación o en los que no se han podido ejecutar durante un período especificado. Para obtener más información acerca del uso de SMS en la fase de valoración, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

#### Analizar la integridad de los datos del inventario

Una vez que se lleva a cabo la auditoría, los administradores deben comprobar que los resultados estén completos y asegurarse de que todos los equipos administrados hayan notificado información actualizada. Se deben realizar las siguientes actividades:

-   Los resultados de la auditoría se deben comparar con una auditoría anterior y se debe observar un aumento o reducción de equipos detectados. Un cambio considerable en los recuentos en comparación con las auditorías anteriores puede indicar un problema de integridad.
-   Los resultados de auditoría también se deben comparar con los objetos de equipo (cuentas de equipo) en los dominios de servicio de directorio de Microsoft Active Directory. Siempre que las cuentas no actualizadas se depuren, será tan útil como realizar la comparación con los servicios de resolución de nombres.
-   Los sistemas en uso activo registrarán y usarán los servicios de resolución de nombres, WINS (servicio de nombres Internet de Windows) y DNS (sistema de nombres de dominio), en su entorno. Los scripts que hacen referencia cruzada a infraestructura activa, como estos servicios, pueden ofrecer una visión integral de lo completo que puede estar el inventario para la administración de actualizaciones. Asegúrese de que la depuración de registros no actualizados esté activada en sus servidores de resolución de nombres para obtener resultados más exactos.

Si el análisis demuestra una discrepancia en la información devuelta, debe investigar más para determinar la causa y realizar los pasos necesarios para asegurarse de que los sistemas que no se tomaron en cuenta en la auditoría se incluyan en la siguiente ejecución de auditoría.

### Determinar la línea de base de su entorno

Una línea de base es un conjunto de configuraciones documentadas de un producto o sistema que se establece en un punto específico en el tiempo. Las bases establecen un estándar con el que los sistemas de la misma clase y categoría deben coincidir. Las operaciones de TI efectivas usan las líneas de base como un punto confiable a partir del cual se integran e implementan los sistemas. Generalmente, la configuración definida por una línea de base se comprueba y se certifica mediante el proveedor de manera estricta.

Una línea de base de software o aplicación proporciona la información necesaria para restaurar un sistema a un estado deseado. Puede ser necesario establecer líneas de base para diferentes aplicaciones de software, proveedores de hardware o tipos de equipo.

La determinación de las líneas de base requiere que realice y mantenga un inventario exacto de los equipos y servicios de su entorno. Recuerde los siguientes puntos cuando establezca las líneas de base de su entorno:

-   La infraestructura que está debajo de la línea de base se debe tratar mediante la administración de problemas. Debe hacer que todos los equipos que se hayan identificado debajo de la línea de base lleven a cabo el cumplimiento. Estos equipos pueden haber tenido problemas con la distribución, programaciones o permisos, o pueden necesitar atención especial a través del control de excepciones.
-   La infraestructura que excede la línea de base no necesariamente supone una ventaja. Los equipos que excedan la línea de base de su clase se deben comprobar para determinar si se han realizado cambios no autorizados. En algunos casos, es posible que sea necesario devolver un sistema a un nivel confiable o puede ser apropiado controlarlo a través de una inmovilización de cambio. Los sistemas que exceden una línea de base aprobada incluyen versiones de aplicaciones o actualizaciones de software cuya interoperabilidad no se ha probado y que las operaciones de TI y la seguridad de TI no han aprobado formalmente.
-   Determinados sistemas tienen circunstancias especiales que los hacen estar exentos de la línea de base de su clase. Por ejemplo, una estación de trabajo antigua con una aplicación de nómina heredada que se conecta a una agencia de procesamiento mediante un módem puede requerir un nivel de sistema operativo muy inferior a la línea de base establecida. Puede que no sea adecuado actualizar este sistema a la línea de base más reciente debido a que podría no ejecutarse la aplicación heredada.

[](#mainsection)[Principio de la página](#mainsection)

Valorar las amenazas y vulnerabilidades de seguridad
----------------------------------------------------

Cuando conozca los equipos y los datos que se han implementado en el entorno de producción, debe llevar a cabo la valoración de seguridad continua para determinar los pasos que debe realizar para proteger la disponibilidad, la integridad y la confidencialidad de los datos y los equipos. Como mínimo, la valoración de seguridad debe abarcar lo siguiente:

-   Identificación de los estándares y las directivas de seguridad.
-   Determinación de cómo se deben aplicar las directivas y los estándares de seguridad.
-   Análisis de las vulnerabilidades del sistema.

Para obtener información más detallada acerca de la realización de una valoración de seguridad, consulte la guía de administración de riesgos de seguridad en [http://www.microsoft.com/technet/security/topics/complianceandpolicies/secrisk/srsgch01.mspx](http://www.microsoft.com/technet/solutionaccelerators/msf/default.mspx).

### Identificar los estándares y directivas de seguridad

Una directiva de seguridad efectiva debe identificar los estándares de seguridad mínimos para el equipo y contribuir a reducir la exposición a posibles vulnerabilidades de seguridad. Para ser eficaz, la directiva de seguridad de una organización se debe revisar cada vez que se efectúen cambios en los sistemas de TI y en el software en el entorno de producción y debe incluir, como mínimo, los siguientes elementos:

-   Estándares de instalación, descripción de métodos y ubicaciones de instalación que se admiten.
-   Estándares de red y dominio, indicando cómo se asignan los nombres y la información de TCP/IP y equipos de dominio que se deben unir.
-   Opciones de seguridad del sistema operativo y configuración de directivas, incluso las que reducen puertos abiertos basados en los servicios necesarios.
-   Cualquier estándar que describa el uso de sistemas de archivos cifrados.
-   Cumplimiento de Service Pack o actualización de software mínimo, actualizado con cada versión de seguridad.
-   Cumplimiento de software antivirus.
-   Parámetros de configuración de seguridad de la aplicación, tales como protección de archivos de macros y zonas de seguridad.
-   Estándares de cuenta administrativa, tales como cambiar nombres o deshabilitar cuentas y configurar cuentas señuelo.
-   Estándares de contraseña segura.

Una infracción de una directiva de seguridad sugiere una vulnerabilidad que se debe eliminar del entorno. La vulnerabilidad puede ser un equipo que no cuenta con varias actualizaciones de software o que no está configurado correctamente, o bien un usuario que no usa contraseñas seguras.

La directiva de seguridad puede ofrecer instrucciones para cada tipo de infracción de cumplimiento de la directiva; ésta se puede usar para determinar la gravedad de la incidencia de una vulnerabilidad específica.

**Nota:** MBSA examina las actualizaciones de seguridad y las configuraciones de seguridad incorrectas habituales. No examina el cumplimiento de todos los elementos de una directiva de seguridad de una organización.

Después de establecer y activar una directiva de seguridad que defina los estándares de seguridad del equipo, debe aplicar las estrategias presentadas en la siguiente sección para tratar cualquier infracción o vulnerabilidad descubierta a través de una serie de transferencias de incidencias.

### Determinar cómo se deben aplicar las directivas y estándares de seguridad

Aplicar una directiva de seguridad puede resultar complicado por la administración distribuida y los activos vulnerables que no se administran centralizadamente. Para los responsables de administrar los activos y resolver la vulnerabilidad puede ser algo desconocido o difícil de encontrar, puede estar en otro departamento de la organización o pueden no contar con los conocimientos necesarios para resolver la vulnerabilidad por sus propios medios.

En consecuencia, hay varias prácticas que son necesarias y útiles al aplicar la directiva de seguridad:

-   Las directivas de seguridad, plazos de cumplimiento y enfoques deben tener el respaldo del equipo directivo en toda la organización.
-   Las técnicas y las herramientas para determinar la propiedad e información administrativa de un equipo no administrado deben estar disponibles para determinados técnicos del departamento de servicios.
-   Los técnicos del departamento de servicios deben tener conocimientos para mitigar cada una de las vulnerabilidades que infringen la directiva de seguridad.
-   Las herramientas y las técnicas automatizadas, como Directiva de grupo, se deben usar para garantizar que los sistemas informáticos cumplen continuamente con la directiva y estándares de seguridad corporativos.

La naturaleza de la vulnerabilidad de seguridad, como el riesgo de vulnerabilidad y el costo de recuperación, deben servir para determinar lo agresiva que debe ser la respuesta a un sistema que no cumple. Si los intentos de resolver la vulnerabilidad en el plazo de tiempo requerido no son correctos, puede optar por usar tácticas más agresivas, entre las que se incluyen:

-   Transferir el problema a la organización del infractor.
-   Deshabilitar la cuenta principal que se usa para obtener acceso al equipo.
-   Retirar el equipo de la red mediante su desconexión física o configurar el hardware de red para que quite automáticamente el dispositivo de la red al deshabilitar puertos, por ejemplo.

Estas dos últimas tácticas generalmente serán motivo de una llamada a servicio técnico, donde la vulnerabilidad no resuelta se puede discutir y se puede determinar una resolución aceptable. Asegúrese de tener apoyo ejecutivo para la directiva de seguridad antes de transferir las infracciones de seguridad e intentar estas técnicas.

### Analizar las vulnerabilidades del sistema

El examen continuo y la notificación de problemas de seguridad son fundamentales para garantizar que se identifiquen y traten las posibles vulnerabilidades de seguridad.

Como mínimo, las organizaciones deben realizar las siguientes acciones:

-   Realice las comprobaciones de las configuraciones que puedan poner en peligro la seguridad en los equipos implementados en el entorno de producción y compruebe el sistema operativo y otros componentes instalados, como Microsoft Internet Information Server (IIS) y Microsoft SQL Server™. Puede usar MBSA para identificar muchas configuraciones incorrectas de seguridad, pero también debe consultar el sitio web de Microsoft Security Central para obtener más información sobre la protección y seguridad de equipos. El sitio se encuentra en [ttp://www.microsoft.com/security](http://www.microsoft.com/security).

-   Examine e identifique regularmente los equipos que puedan estar infectados por un virus. Puede crear estos informes con las herramientas antivirus que su organización ha seleccionado.
-   Revise la información devuelta por las herramientas de control de red, registros de eventos y otras herramientas de supervisión, así como el resultado de cualquier sistema de detección de intrusos para determinar si existen ataques contra los equipos en el entorno de producción.
-   Cree y mantenga las imágenes del sistema operativo (líneas de base) que se puedan aplicar a una plataforma de hardware determinada para revertir rápidamente un sistema en peligro a un sistema operativo correcto conocido.
-   Compruebe que todos los usuarios y administradores conozcan los pasos que necesitan realizar en caso de un ataque a equipos en el entorno de producción.
-   Mantenga una lista por prioridades de toda la información clave y activos que necesita proteger en primer lugar si se produce un ataque.
-   Compruebe los registros y configuraciones del enrutador y el firewall para asegurarse de que son coherentes con los estándares determinados de la organización para estos dispositivos.
-   Revise las instrucciones de seguridad del controlador de dominio.

El examen de posibles vulnerabilidades de seguridad de los sistemas debe ser lo más automatizado posible y se debe realizar con regularidad; diariamente en la mayoría de los sistemas. La frecuencia dependerá del nivel de automatización con que cuente para cada una de estas áreas, la disponibilidad y los conocimientos del personal de seguridad de TI en la organización y el nivel de compromiso por un entorno seguro.

Si descubre que se ha aprovechado una vulnerabilidad de seguridad, debe llevar a cabo un proceso de respuesta de emergencia para reducir las consecuencias.

[](#mainsection)[Principio de la página](#mainsection)

Determinar la mejor fuente de información acerca de las actualizaciones de software
-----------------------------------------------------------------------------------

Cuando conozca lo que ha implementado en su entorno de producción y haya evaluado las amenazas y vulnerabilidades de seguridad, debe determinar la mejor fuente de información acerca de las nuevas actualizaciones de software. Esta información se usará en la siguiente fase al identificar las nuevas actualizaciones de software. Las fuentes de información acerca de las actualizaciones de software pueden ser:

-   Notificaciones por correo electrónico.
-   Sitios web.
-   Representantes técnicos de Microsoft.

Suscribirse a los métodos de notificación apropiados es fundamental para mantener y actualizar sus líneas de base de operación establecidas y para implementar un proceso eficaz de administración de actualizaciones.

En Microsoft Security Response Center (MSRC) se investigan los problemas que se notifican directamente a Microsoft, así como los problemas tratados en determinados grupos de noticias de seguridad populares. Los boletines de seguridad que Microsoft publica incluyen información que describe las vulnerabilidades y los productos afectados. Los boletines también incluyen información técnica detallada que describe vulnerabilidades, actualizaciones y soluciones, así como las consideraciones de implementación y descarga de instrucciones para cualquier actualización disponible.

Los boletines de seguridad y actualizaciones de seguridad relacionadas se publican mensualmente el segundo martes del mes entre las 10 a.m. y las 11 a.m. hora del Pacífico, a menos que Microsoft determine que los clientes recibirán un mejor servicio si publica un boletín de seguridad a una hora diferente. Esta directiva se estableció como respuesta a los comentarios de clientes internacionales, con el objetivo de permitirles programar los planes de administración de actualizaciones.

Puede revisar todos los boletines de seguridad y cualquier otro tipo de información acerca de la seguridad de los productos de Microsoft en <http://www.microsoft.com/technet/security/default.mspx>. Todas las actualizaciones de seguridad incluidas en los dos últimos Service Packs para los productos actualmente compatibles están disponibles para su descarga en esta ubicación.

Puede obtener información acerca de las nuevas actualizaciones de software de Microsoft mediante mensajes de correo electrónico. El nivel de detalle que necesite dependerá del tamaño de su organización y del nivel de información técnica que desee, de la siguiente forma:

-   Para los clientes que tienen amplios conocimientos o interés en la tecnología subyacente en las actualizaciones de seguridad, Microsoft TechNet ofrece Microsoft Security Notification Service. Se trata de un servicio de notificación gratuito por correo electrónico dirigido a los profesionales de TI. Los mensajes de correo electrónico incluyen información técnica detallada. Para obtener más información o suscribirse para recibir Microsoft Security Notification Service, consulte <http://www.microsoft.com/technet/security/bulletin/notify.mspx>.

-   Microsoft ofrece Microsoft Security Update, un servicio de alerta por correo electrónico gratuito que permite que las pequeñas empresas se mantengan informadas de las últimas actualizaciones de seguridad. Cada vez que Microsoft publica una actualización, los suscriptores reciben un mensaje de correo electrónico que explica en términos no técnicos los motivos por los que Microsoft publica la actualización. El mensaje también enumera los productos que están afectados y proporciona un vínculo al anuncio completo en el sitio web de Security Central. Puede suscribirse para recibir Microsoft Technical Security Notifications en [https://profile.microsoft.com/RegSysProfileCenter/subscriptionwizard.aspx?wizid=5a2a311b-5189-4c9b-9f1a-d5e913a26c2e&lcid=1033](https://profile.microsoft.com/regsysprofilecenter/subscriptionwizard.aspx?wizid=5a2a311b-5189-4c9b-9f1a-d5e913a26c2e&lcid=1033).

-   También puede recibir notificaciones de los nuevos artículos de Knowledge Base a través del registro para el boletín gratuito TechNet Flash en <http://www.microsoft.com/technet/abouttn/subscriptions/flash_register.mspx>. Estos artículos contendrán con frecuencia información acerca de las actualizaciones de software que debe implementar para resolver los problemas de su entorno de producción.

[](#mainsection)[Principio de la página](#mainsection)

Valorar la infraestructura de distribución de software existente
----------------------------------------------------------------

La valoración de la infraestructura de distribución del software constituye otra parte principal de un proceso de administración de actualizaciones efectivo. La valoración debe tratar interrogantes como los siguientes:

-   ¿Existe una infraestructura de distribución de software?
-   ¿Se puede usar para distribuir actualizaciones de software?
-   ¿Ofrece servicio a todos los equipos de su entorno? ¿Se ha diseñado para administrar la actualización de los equipos críticos para la empresa?
-   ¿Se mantiene de forma adecuada la implementación de la infraestructura de WSUS o SMS, Active Directory y Directiva de grupo?

Si usa WSUS, debe configurar un servidor principal WSUS individual para descargar automáticamente las actualizaciones de software de los servidores públicos Windows Update de Microsoft. Estas actualizaciones se deben realizar diariamente mediante una programación de sincronización preconfigurada. Después de que las actualizaciones se hayan aprobado, estarán inmediatamente disponibles para todos los clientes WSUS. Se debe configurar que la actualización se descargue en horas sin mucho movimiento en la red. Para obtener información más detallada acerca del uso de WSUS en la fase de valoración, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true).

Si usa SMS, observe que los servidores de sitio deben encontrarse donde hay una gran población de clientes o donde son necesarios para administrar o controlar el ancho de banda de la red. En ciertas ubicaciones, puede necesitar dos servidores de sitio SMS; uno para admitir clientes de estación de trabajo y otro para admitir equipos críticos para la empresa.

### Más información

Para obtener información más detallada acerca de WSUS en la fase de valoración, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true).

Para obtener información más detallada acerca del uso de SMS y SMS 2003 en la fase de valoración, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

[](#mainsection)[Principio de la página](#mainsection)

Valorar la eficacia operativa
-----------------------------

Los procesos operativos de TI efectivos son quizás el aspecto de dependencia más importante del cual depende la administración efectiva de actualizaciones. Microsoft Operations Framework (MOF), basado en ITIL (biblioteca de infraestructuras de TI), detalla las 20 funciones de administración de servicio (SMF). Para obtener más información sobre esas SMF que tienen un efecto directo en la administración de actualizaciones, incluida la administración de cambios, la administración de configuración y la administración de versiones de lanzamiento, consulte la guía de TechNet de soluciones Microsoft para administración en TechNet en [http://www.microsoft.com/technet/itsolutions/cits/mo/default.msp](http://www.microsoft.com/technet/itsolutions/cits/mo/default.mspx).

Existen varias preguntas que debe plantearse al valorar su eficacia operativa en el contexto de estas SMF:

-   ¿Cuenta con personal lo suficientemente preparado para realizar la administración de actualizaciones?
-   ¿El personal sabe que es necesaria la administración de actualizaciones?
-   ¿Los responsables comprenden la configuración de seguridad, las vulnerabilidades informáticas comunes, las técnicas de distribución de software, la administración remota y el proceso de administración de actualizaciones?
-   ¿Existen procesos operativos estándar o son operaciones diarias muy indefinidas e imprecisas?
-   ¿Existen procesos para la administración de cambios y administración de versiones de lanzamiento, incluso informales? La protección de un entorno de los ataques no se debe dejar al azar ni debe ser una serie de operaciones que se llevan a cabo a medida que se necesitan.
-   ¿Existe un proceso de emergencia para implementar actualizaciones de software?
-   ¿Se evalúan y se comprueban los procesos continuamente?

La administración de actualizaciones es una de las muchas áreas de operaciones de TI. Las organizaciones gastan un porcentaje considerable de sus presupuestos de TI en operaciones, ya que lograr la excelencia operativa reduce el gasto y a la vez mejora la confiabilidad, la disponibilidad, la compatibilidad y la administración de servicios importantes.

Una valoración de operaciones permite que el personal de operaciones aprecie los beneficios tangibles para las operaciones existentes o propuestas, independientemente del tamaño de la empresa o su nivel de madurez.

Para obtener una autoevaluación rápida de la excelencia operativa de su organización, consulte MOF Self-Assessment Tool en <http://www.microsoft.com/technet/itsolutions/cits/mo/mof/moftool.mspx>.

Para obtener más información acerca de las valoraciones de operaciones y para encontrar servicios de consultoría que puedan realizar una valoración de las operaciones, consulte MOF Operations Assessment Service Offering en [http://www.microsoft.com/services/microsoftservices/srv\_mgmt\_ops.mspx](http://technet.microsoft.com/es-es/library/bb887502.aspx).

### Modelo de administración

Una organización también debe revisar el modelo de administración actual de su entorno de TI y determinar en qué medida sirve a la administración de actualizaciones. A continuación se enumeran algunas de las cuestiones que debe tener en cuenta:

-   ¿Qué tamaño presenta la infraestructura en comparación con la cantidad de personal? ¿Cuál es la relación administrador-sistema?
-   ¿Cuál es el modelo de compatibilidad actual: centralizado, descentralizado o compartido?
-   ¿Qué horas de servicio ofrece el personal de soporte técnico? ¿Hay suficientes lapsos de cambio asignados para mantenimiento y administración?
-   ¿Están definidas claramente las funciones y se comunican a los miembros del equipo?
-   ¿Se han formalizado y se siguen los procesos de administración de servicios?
-   ¿Se cuenta con suficientes herramientas para que el personal lleve a cabo sus funciones?

### Conjuntos de habilidades

Las siguientes preguntas pueden ayudarle a determinar los conjuntos adecuados de habilidades requeridas para la ejecución de la administración de actualizaciones efectiva.

-   ¿Se cuenta con suficiente experiencia en el manejo del tamaño y la complejidad de la infraestructura?
-   ¿El personal dispone de los conocimientos adecuados y con las tecnologías relevantes?
-   ¿Se trabaja en equipo?
-   ¿Se cuenta con la experiencia o preparación apropiada para comprender las disciplinas y metodologías operativas clave?
-   ¿Se tienen conocimientos de scripts?
-   ¿Se comprenden los permisos del sistema y de usuario y los contextos?
-   ¿Se comprenden las estructuras y dependencias de actualización de software?

[](#mainsection)[Principio de la página](#mainsection)

Resumen
-------

Estos son los puntos clave para recordar de la fase de valoración del proceso de administración de actualizaciones:

-   Se deben determinar las amenazas y vulnerabilidades del entorno de producción.
-   Se deben conocer cuáles son los activos críticos para la empresa.
-   Se deben conocer los elementos implementados en el entorno de producción y qué se clasifica como administrado (mediante herramientas de administración) y lo que no.
-   Se debe garantizar que las herramientas de distribución de software estén configuradas, reciban mantenimiento y puedan admitir la administración de actualizaciones normal y de emergencia.
-   Se debe garantizar que el personal tiene asignadas funciones y responsabilidades y que saben cómo responder en caso de emergencia; es decir, cómo afrontar la actualización de software y cómo mitigar sus repercusiones.

[](#mainsection)[Principio de la página](#mainsection)

Paso a la fase de identificación
--------------------------------

La activación para el paso a la fase de identificación del proceso de administración de actualizaciones es la notificación de que existe una nueva actualización de software. Para obtener más información acerca de la fase de identificación, consulte el módulo "[Fase 2 de la administración de actualizaciones: Identificación](https://technet.microsoft.com/es-es/library/dc3893d5-6e12-443a-9e7d-f2b999b4bff2(v=TechNet.10))".

[Principio de la página](#mainsection)

**Descargar la solución completa**

[Administración de revisiones con SMS 2003](http://www.microsoft.com/downloads/details.aspx?familyid=959ee7d6-7ddf-409a-9522-7d270bdcf12a&displaylang=en)

[](#mainsection)[Principio de la página](#mainsection)
