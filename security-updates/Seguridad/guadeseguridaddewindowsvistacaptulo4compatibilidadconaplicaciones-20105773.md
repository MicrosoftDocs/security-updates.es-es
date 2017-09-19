---
TOCTitle: 'Guía de seguridad de Windows Vista, Capítulo 4: Compatibilidad con aplicaciones'
Title: 'Guía de seguridad de Windows Vista, Capítulo 4: Compatibilidad con aplicaciones'
ms:assetid: 'd11f3fd0-b74e-4e77-bff9-4e1b8e5d1d68'
ms:contentKeyID: 20105773
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Bb629463(v=MSDN.10)'
---

Guía de seguridad de Windows Vista
==================================

### Capítulo 4: Compatibilidad con aplicaciones

Publicado: noviembre 8, 2006

La compatibilidad con aplicaciones constituye siempre un reto fundamental e importante al que las organizaciones deben enfrentarse al implementar un nuevo sistema operativo. Gran parte de los esfuerzos de implementación para Windows Vista™ conllevaba garantizar que las características y servicios nuevos del sistema operativo mantuvieran un alto grado de funcionalidad y compatibilidad con los programas más antiguos. Durante la implementación, el equipo Microsoft Application Experience Team probó muchas aplicaciones de una gran variedad de proveedores de terceros.

La configuración de seguridad recomendada en esta guía para reforzar Windows Vista se ha probado de forma exhaustiva para que sea compatible con el sistema operativo central, así como con el conjunto de aplicaciones de Microsoft® Office. Las aplicaciones que se ejecutan en Windows Vista deben seguir funcionando correctamente en los equipos cliente sujetos a las recomendaciones de configuración de esta guía.

No obstante, cabe la posibilidad de que aplicaciones más antiguas no puedan funcionar correctamente con algunas de las tecnologías de seguridad nuevas integradas en Windows Vista. Las tecnologías Control de cuentas de usuario (UAC) y Protección de recursos de Windows pueden interferir con aplicaciones más antiguas.

El Acelerador de Solución Microsoft para la implementación de escritorio en la empresa (BDD) 2007 contiene amplias instrucciones de compatibilidad con aplicaciones para permitir a los profesionales de TI que prueben dicha compatibilidad con Windows Vista y mitiguen los problemas correspondientes que surjan durante el proceso. Para obtener más información, consulte la [*Guía del equipo de compatibilidad con aplicaciones*](http://go.microsoft.com/fwlink/?linkid=74194) (en inglés) en Microsoft TechNet®.

Este capítulo incluye procedimientos sencillos que se pueden usar para probar el nivel de compatibilidad de las aplicaciones con Windows Vista, trata algunas de las causas más habituales de los problemas de compatibilidad con aplicaciones y ofrece vínculos a recursos disponibles que pueden ayudarle a tratar dichos problemas.

##### En esta página

[](#edaa)[Comprobación de compatibilidad en treinta minutos](#edaa)
[](#ecaa)[Problemas conocidos de compatibilidad con aplicaciones](#ecaa)
[](#ebaa)[Herramientas y recursos](#ebaa)
[](#eaaa)[Más información](#eaaa)

### Comprobación de compatibilidad en treinta minutos

Esta sección ofrece instrucciones sobre cómo probar y evaluar la compatibilidad de aplicaciones con Windows Vista. Incluye dos escenarios que puede usar para probar la compatibilidad de aplicaciones con el sistema operativo. Le ayudarán a:

-   Probar una aplicación con una instalación limpia de Windows Vista.

-   Probar una aplicación con una actualización a Windows Vista a partir de Microsoft Windows® XP con Service Pack 2 (SP2).

**Para probar una aplicación con una instalación limpia de Windows Vista**

1.  Instale Windows Vista en un equipo de prueba.

2.  Inicie sesión como administrador en el equipo de prueba con Windows Vista.

3.  Instale la aplicación que desee probar con Windows Vista. Si aparece una confirmación que solicita permiso para instalar la aplicación, haga clic en **Permitir** para continuar la instalación. Si la instalación se realiza correctamente, vaya al paso 6.

4.  Si no se puede realizar la instalación de la aplicación y no se muestra ninguna confirmación de permiso, haga clic con el botón secundario en el archivo .exe del instalador, haga clic en la opción **Ejecutar este programa como administrador** y vuelva a instalar la aplicación. Si la instalación se realiza correctamente, vaya al paso 7.

    **Nota**   Este paso no es necesario si usa el archivo de Microsoft Installer (.msi) para instalar la aplicación.

5.  Si recibe algún error relacionado con la versión del sistema operativo, el registro de la aplicación o la copia del archivo, haga clic con el botón secundario en el archivo .exe del instalador, haga clic en **Compatibilidad** y, a continuación, elija el modo de compatibilidad de Windows XP SP2.

6.  Repita el paso 2. Si sigue sin poder instalar la aplicación, vaya al paso 8.

7.  Inicie sesión como usuario sin privilegios administrativos para probar el equipo con Windows Vista.

8.  Inicie la aplicación. Si la aplicación no se inicia correctamente o muestra errores, habilite el modo de compatibilidad de Windows XP SP2 para el archivo .exe de la aplicación y, a continuación, intente instalarlo de nuevo en el sistema operativo.

9.  Si la aplicación se inicia correctamente, ejecute el conjunto completo de pruebas que normalmente usaría para probar la aplicación en un equipo con Windows XP. Compruebe la funcionalidad de la aplicación para confirmar que funciona correctamente. Si la aplicación pasa todas las pruebas de funcionalidad principales, significa que funciona correctamente en Windows Vista.

10. Si la aplicación no se instala ni inicia correctamente, deja de responder, encuentra un error o no se realiza alguna de las pruebas de funcionalidad principales, es posible que sea una de las pocas aplicaciones que presentan problemas de compatibilidad con Windows Vista. Consulte el resto de recursos de referencia de este capítulo para seguir investigando y probando la aplicación.

**Para probar una aplicación con una actualización a Windows Vista a partir de Windows XP SP2**

1.  Instale Windows XP con SP2 en un equipo de prueba y, a continuación, instale la aplicación que desee probar. Compruebe toda la funcionalidad de la aplicación antes de continuar.

2.  Actualice el equipo de prueba a Windows Vista. Siga las instrucciones de configuración y actualización de Windows Vista. Una vez que finalice la actualización, inicie sesión en el equipo de prueba de igual forma que un equipo con Windows XP.

3.  Inicie la aplicación. Si la aplicación no se inicia correctamente o si aparecen errores, habilite el modo de compatibilidad de Windows XP SP2 para el archivo .exe de la aplicación y pruebe a instalarla de nuevo.

4.  Si la aplicación se inicia correctamente, ejecute el conjunto completo de pruebas que normalmente usaría para probar la aplicación en un equipo con Windows XP. Compruebe la funcionalidad de la aplicación para confirmar que funciona correctamente. Si la aplicación pasa todas las pruebas de funcionalidad principales, significa que funciona correctamente en Windows Vista.

5.  Si la aplicación no se instala ni inicia correctamente, deja de responder, encuentra un error o no se realiza alguna de las pruebas de funcionalidad principales, es posible que sea una de las pocas aplicaciones que presentan problemas de compatibilidad con los cambios de Windows Vista. Consulte el resto de recursos de referencia de este capítulo para seguir investigando y probando la aplicación.

Si lleva a cabo estos escenarios y determina que la aplicación funciona correctamente, puede suponer que también funcionará con Windows Vista.

[](#mainsection)[Principio de la página](#mainsection)

### Problemas conocidos de compatibilidad con aplicaciones

Esta sección describe algunas de las tecnologías nuevas, mejoras y cambios de Windows Vista más comunes que se ha comprobado que producen problemas de compatibilidad con aplicaciones. Siempre que sea posible, esta sección también incluye formas potenciales de mitigar dichos problemas.

**Importante**   Pruebe todas las aplicaciones de terceros que tenga intención de usar en el entorno con Windows Vista para asegurarse de que funcionarán correctamente con el sistema operativo.

#### Mejoras de seguridad

Las siguientes mejoras de seguridad nuevas de Windows Vista pueden provocar problemas de compatibilidad con aplicaciones de terceros:

-   **Control de cuentas de usuario**. Esta nueva característica ofrece un método de separación de las tareas y los privilegios de usuario estándar de aquéllos que requieren el acceso como administrador. UAC aumenta la seguridad mejorando la experiencia del equipo para los usuarios con cuentas de usuario estándar. Ahora los usuarios pueden realizar más tareas y disfrutar de una mayor compatibilidad con aplicaciones sin necesidad de iniciar sesión en sus equipos cliente con privilegios de administrador. Esto permite reducir la incidencia de software malintencionado, instalaciones de software no autorizado y cambios del sistema no aprobados.

    UAC puede presentar problemas en aplicaciones que no sean compatibles con esta mejora tecnológica. Por este motivo, es importante probar aplicaciones habilitadas para UAC antes de implementarlas. Para obtener más información sobre la prueba de compatibilidad de aplicaciones, consulte la [*Guía del equipo de compatibilidad con aplicaciones*](http://go.microsoft.com/fwlink/?linkid=74194) (en inglés) de BDD en TechNet.

-   **Protección de recursos de Windows**. Esta nueva característica de Windows Vista ayuda a proteger los archivos del sistema y las ubicaciones de registro protegidas con el fin de mejorar la seguridad y la estabilidad generales del sistema operativo. La mayoría de las aplicaciones que antes podían tener acceso o modificar estas ubicaciones, se redirigen automáticamente a ubicaciones temporales, que pueden usar para continuar funcionando sin problemas.

    No obstante, las aplicaciones que necesitan acceso completo a estas áreas protegidas y no pueden controlar el proceso de redirección automática, no funcionarán correctamente con Windows Vista. En estos casos, debe modificar las aplicaciones para que funcionen de manera adecuada. Para obtener información sobre esta nueva característica y sus implicaciones con respecto a la compatibilidad con aplicaciones, consulte [Acerca de la Protección de recursos de Windows](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/wfp/setup/about_windows_file_protection.asp) (en inglés) en Microsoft MSDN®.

-   **Modo protegido**. Esta nueva característica de Microsoft Internet Explorer® 7 ayuda a proteger los equipos en los que se ejecute Windows Vista frente a la instalación de software malintencionado u otro software perjudicial, gracias a la ejecución del sistema operativo con menos derechos y mayor seguridad. Cuando Internet Explorer está en modo protegido, el explorador sólo puede interactuar con áreas muy específicas del sistema de archivos y del registro.

    Aunque el modo protegido ayuda a mantener la integridad de los equipos cliente en los que se ejecute Windows Vista, puede afectar al funcionamiento correcto de aplicaciones más antiguas de Internet y aplicaciones Web de intranet. Es posible que necesite modificar dichas aplicaciones Web para ejecutarlas en un entorno más restrictivo.

#### Cambios e innovaciones del sistema operativo

Los siguientes cambios nuevos e innovaciones del sistema operativo Windows Vista pueden provocar problemas de compatibilidad con aplicaciones de terceros:

-   **Nuevas API de sistema**. Las interfaces de programación de aplicaciones (API) exponen capas del sistema operativo Windows Vista de forma diferente a las versiones anteriores de Windows. Los software antivirus y firewall son ejemplos de aplicaciones que se basan en estas nuevas API para controlar y proteger Windows Vista. Debe actualizar las aplicaciones que realicen estas funciones a las versiones que sean compatibles con Windows Vista.

-   **Windows** **Vista de 64 bits**. Las aplicaciones de 16 bits y los controladores de 32 bits no son compatibles con el entorno de 64 bits de Windows Vista. La redirección automática de archivos del sistema y el registro no está disponible para el entorno de 64 bits. Por ello, las nuevas aplicaciones de 64 bits deben cumplir los estándares de aplicación de Windows Vista.

-   **Versiones del sistema operativo**. Numerosas aplicaciones más antiguas comprueban versiones específicas de Windows. Si las aplicaciones de terceros no pueden detectar alguna versión de sistema operativo específica, muchas de ellas dejan de responder.

    La mayoría de los requisitos de versión de sistema operativo relacionados con problemas de seguridad están resueltos con la nueva funcionalidad integrada en Windows Vista. Características como el Asistente para la compatibilidad de programas pueden resolver normalmente este tipo de problemas de forma automática. Para obtener más información sobre el Asistente para la compatibilidad de programas y otras herramientas y recursos, consulte la siguiente sección de este capítulo.

El artículo [Historia de los desarrolladores de Windows Vista: libro de instrucciones de compatibilidad con aplicaciones](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dnlong/html/appcomp.asp) (en inglés) de MSDN ofrece información adicional sobre estas mejoras de seguridad, así como sobre los cambios e innovaciones del sistema operativo Windows Vista. También incluye métodos de prueba y posibles remedios a estos problemas de compatibilidad.

[](#mainsection)[Principio de la página](#mainsection)

### Herramientas y recursos

Esta sección ofrece información general y vínculos a distintas características y tecnologías disponibles para Windows Vista que están diseñadas para ayudarle a resolver problemas de compatibilidad.

#### Asistente para la compatibilidad de programas

Esta característica especifica automáticamente un "modo de compatibilidad" adecuado para aplicaciones diseñadas para ejecutarse en versiones anteriores de Windows. Cuando Windows Vista detecta aplicaciones que necesitan ejecutarse en modos de compatibilidad de Windows XP, Windows 2000 o versiones posteriores de Windows, el sistema operativo redirecciona las aplicaciones para que se ejecuten automáticamente en Windows Vista sin necesidad de más intervención por parte del usuario.

Para obtener más información, consulte la página [Asistente para la compatibilidad de programas: preguntas más frecuentes](http://windowshelp.microsoft.com/windows/en-us/help/82c0440d-553e-47e9-b4bd-6c2d10df4de71033.mspx) (en inglés) del sitio Web de ayuda y soporte técnico de Windows Vista.

#### Asistente para compatibilidad de programas

El Asistente para compatibilidad de programas se incluye con Windows Vista para ayudarle cuando un programa escrito a partir de una versión anterior de Windows no se ejecute correctamente. El asistente le ayudará a especificar configuración de compatibilidad para el programa, que resolverá los problemas de compatibilidad de las aplicaciones en la mayoría de los programas más antiguos.

Para tener acceso al Asistente para compatibilidad de programas, haga doble clic en el icono **Asistente para compatibilidad de programas** del escritorio.

Para obtener más información, consulte la página[Hacer que programas más antiguos se ejecuten en esta versión de Windows](http://windowshelp.microsoft.com/windows/en-us/help/bf416877-c83f-4476-a3da-8ec98dcf5f101033.mspx) (en inglés) del sitio Web de ayuda y soporte técnico de Windows Vista.

**Advertencia:**

No ejecute el Asistente para compatibilidad de programas en programas antivirus, utilidades de disco u otros programas del sistema más antiguos, ya que puede producir pérdida de datos o crear riesgos de seguridad. En su lugar, use sólo versiones de estos programas y utilidades diseñados específicamente para funcionar con Windows Vista.

#### Microsoft Standard User Analyzer

Esta herramienta de compatibilidad de aplicaciones permite a desarrolladores y profesionales de TI diagnosticar problemas que impedirán que un programa se ejecute correctamente sin privilegios administrativos. El uso de Standard User Analyzer para probar las aplicaciones permite identificar problemas de acceso a archivos, acceso al registro, símbolos (token) y otras áreas protegidas del sistema operativo.

En Windows Vista, incluso los administradores ejecutan la mayoría de programas con privilegios de usuario estándar. Esta herramienta le permite asegurarse de que la aplicación no obliga a contar con acceso de administrador para poder tener acceso. Los resultados se muestran en una sencilla interfaz gráfica.

Puede descargar esta herramienta desde [Microsoft Standard User Analyzer](http://technet.microsoft.com/en-us/library/cc766021.aspx) en el Centro de descarga de Microsoft.

#### Kit de herramientas de compatibilidad con aplicaciones

Microsoft ha puesto a su disposición un conjunto de herramientas y documentación para ayudarle a identificar y administrar la cartera de aplicaciones de la organización. El kit de herramientas de compatibilidad de aplicaciones (ACT) está diseñado para ayudarle a reducir el costo y el tiempo dedicados a resolver problemas de compatibilidad de aplicaciones, con objeto de permitirle implementar Windows Vista de forma más rápida.

ACT puede ayudarle a preparar Windows Vista detallando el inventario de aplicaciones existentes, administrando aplicaciones esenciales y determinando la extensión del entorno de aplicaciones que puede requerir atención especial para la preparación de Windows** **Vista.

ACT 4.1 está disponible actualmente y se proporcionó para ayudar a los clientes a implementar Windows** **XP SP2. ACT 4.1 examina problemas de Internet Explorer, configuración de firewall e interfaces DCOM. ACT se diseñó para identificar aplicaciones que requieren una mayor comprobación, para identificar las aplicaciones no actualizadas y para determinar qué aplicaciones ya eran compatibles con SP2, lo que permite priorizar los esfuerzos del usuario.

ACT 5.0 se ha actualizado expresamente para admitir las características de seguridad de Windows Vista.

Entre las mejoras de este kit de herramientas, se incluyen:

-   Nuevos evaluadores de compatibilidad específicos de Windows Vista.

-   Una interfaz de usuario actualizada que permite administrar la configuración de evaluadores de forma centralizada.

-   Nuevas características de organización de datos que permiten categorizar y priorizar las aplicaciones.

-   Características de análisis de datos que permiten ver completos informes de compatibilidad.

-   Una comunidad de aplicaciones en línea que permite a los clientes y a los fabricantes independientes de software (ISV) compartir información sobre sus resultados de pruebas de compatibilidad de aplicaciones.

Para obtener más información sobre el kit de herramientas, consulte la página [Compatibilidad de aplicaciones con Windows](http://www.microsoft.com/technet/prodtechnol/windows/appcompatibility/default.mspx) de TechNet.

##### Soluciones temporales

Además de las herramientas y recursos de compatibilidad con aplicaciones específicas, hay disponibles una serie de tecnologías adicionales de Microsoft que puede usar para afrontar problemas de compatibilidad cuya resolución pueda llevar cierto tiempo. Estas tecnologías están diseñadas para ayudarle a migrar a Windows Vista y seguir ejecutando aplicaciones empresariales esenciales que no sean compatibles con Windows Vista. Entre estas tecnologías, se incluyen las siguientes:

-   **Virtual PC**. Puede usar Virtual PC para ejecutar aplicaciones en Windows Vista que sólo funcionen correctamente con versiones más antiguas de Windows. Virtual PC permite a los usuarios tener disponible una versión anterior de Windows para ejecutar aplicaciones que no sean compatibles con el entorno de Windows Vista hasta que se implementen versiones actualizadas de aplicaciones no compatibles. Para obtener más información, consulte el sitio Web [Microsoft Virtual PC](http://www.microsoft.com/windows/virtualpc/default.mspx) (en inglés) en Microsoft.com.

-   **Servicios de Terminal Server para aplicaciones host**. El alojamiento de aplicaciones más antiguas en Servicios de Terminal Server permite ofrecer aplicaciones basadas en Windows o el propio escritorio de Windows de forma virtual a cualquier dispositivo de la red. Los clientes de Windows Vista pueden conectarse a estos entornos de aplicaciones host a través del Escritorio remoto para obtener acceso a aplicaciones más antiguas. Para obtener más información, consulte [Información general técnica de Servicios de Terminal Server de Windows Server 2003](http://www.microsoft.com/windowsserver2003/techinfo/overview/termserv.mspx) (en inglés) en el sitio Web de Microsoft Windows Server 2003 R2.

-   **Virtual Server para aplicaciones host**. Con un entorno de Virtual Server, puede alojar aplicaciones heredadas y permitir la conectividad remota a usuarios finales que necesiten tener acceso a dichas aplicaciones. Junto con Windows Server 2003, Virtual Server 2005 R2 ofrece una plataforma de virtualización que ejecuta la mayoría de sistemas operativos *x*86 principales en un entorno de invitado y que se admite como host en los sistemas operativos Windows Server y en las aplicaciones de Microsoft Windows Server System™. Para obtener más información, consulte [Información del producto Virtual Server 2005 R2](http://www.microsoft.com/windowsserversystem/virtualserver/evaluation/vsoverview.mspx)(en inglés) en el sitio Web de Microsoft Virtual Server.

[](#mainsection)[Principio de la página](#mainsection)

### Más información

Los siguientes vínculos ofrecen información adicional sobre temas de compatibilidad con aplicaciones de Windows Vista:

-   [Acerca de la Protección de recursos de Windows](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/wfp/setup/about_windows_file_protection.asp) (en inglés) en Microsoft MSDN®.

-   [*Guía del equipo de compatibilidad con aplicaciones*](http://go.microsoft.com/fwlink/?linkid=74194) (en inglés) en TechNet.

-   [Introducción a la API de modo protegido](http://msdn.microsoft.com/en-us/library/ms537319.aspx) (en inglés) en MSDN.

-   [Hacer que programas más antiguos se ejecuten en esta versión de Windows](http://windowshelp.microsoft.com/windows/en-us/help/bf416877-c83f-4476-a3da-8ec98dcf5f101033.mspx) (en inglés) en el sitio Web de ayuda y soporte técnico de Windows Vista.

-   [Kit de herramientas de compatibilidad de aplicaciones de Microsoft 5.0](http://www.microsoft.com/technet/windowsvista/appcompat/act5feat.mspx) (en inglés) en TechNet.

-   [Microsoft Standard User Analyzer](http://technet.microsoft.com/en-us/library/cc766021.aspx) (en inglés) en el Centro de descarga de Microsoft.

-   [Soluciones de virtualización de Microsoft](http://www.microsoft.com/windowsserversystem/virtualization/default.mspx) (en inglés) en Microsoft.com.

-   [Asistente para la compatibilidad de programas: preguntas más frecuentes](http://windowshelp.microsoft.com/windows/en-us/help/82c0440d-553e-47e9-b4bd-6c2d10df4de71033.mspx) (en inglés) en el sitio Web de ayuda y soporte técnico de Windows Vista.

-   [Información general técnica de Servicios de Terminal Server de Windows Server 2003](http://www.microsoft.com/windowsserver2003/techinfo/overview/termserv.mspx) (en inglés) en Microsoft.com.

-   [Historia de los desarrolladores de Windows Vista: libro de instrucciones de compatibilidad con aplicaciones](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dnlong/html/appcomp.asp) (en inglés) en MSDN.

-   [Compatibilidad de aplicaciones con Windows](http://www.microsoft.com/technet/prodtechnol/windows/appcompatibility/default.mspx) (en inglés) en TechNet.

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Obtenga la Guía de seguridad de Windows Vista](http://go.microsoft.com/fwlink/?linkid=74028)

**Actualizar notificaciones**

[Suscríbase para obtener información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)

**Opiniones**

[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=windows%20vista%20security%20guide)

[](#mainsection)[Principio de la página](#mainsection)
