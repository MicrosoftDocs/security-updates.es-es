---
TOCTitle: 'Data Encryption Toolkit for Mobile PCs: Capítulo 5: Elección de la solución correcta'
Title: 'Data Encryption Toolkit for Mobile PCs: Capítulo 5: Elección de la solución correcta'
ms:assetid: 'b77d6369-10e9-4e66-8c67-c9f8cb073ced'
ms:contentKeyID: 20200220
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162816(v=TechNet.10)'
---

Data Encryption Toolkit for Mobile PCs: análisis de seguridad
=============================================================

### Capítulo 5: Elección de la solución correcta

Publicado: abril 4, 2007

Para elegir la mejor combinación de tecnologías de cifrado, necesita comprender los riesgos para los datos que necesitan protección. Después puede asignar un valor a esos datos (asegurándose de que incluye los costos directos e indirectos) y elegir una solución que proporcione la mejor rentabilidad de la inversión al tiempo que se proporciona un nivel adecuado de protección.

La tabla Resumen de minimización de riesgos enumera los riesgos para los datos e indica si las combinaciones de las tecnologías de cifrado descritas en esta guía resultan eficaces en su minimización. Los riesgos que se pueden minimizar con opciones específicas están marcados con la letra **Y**. Los guiones **-** indican riesgos para los que la opción específica proporciona poca o ninguna minimización de riesgos.

**Tabla 5.1. Resumen de minimización de riesgos**

![](images/Cc162816.865b473f-87a8-459c-80f3-79361863d073(es-es,TechNet.10).gif)
##### En esta página

[](#ecaa)[Uso de la tabla Resumen de minimización de riesgos](#ecaa)
[](#ebaa)[Conclusión](#ebaa)

### Uso de la tabla Resumen de minimización de riesgos

La tabla se puede usar para seleccionar las tecnologías adecuadas y las configuraciones que necesita implementar para lograr el estado de seguridad deseado en la organización. Como las directivas y la configuración del sistema operativo también afectan a las tecnologías de cifrado, la tabla y los riesgos se pueden usar para comprender el impacto que otra directiva de seguridad puede tener en la solución de cifrado.

Por ejemplo, en la tabla se puede observar que para casi toda las opciones, la organización debe actuar para configurar la funcionalidad "reanudar desde el modo en espera" a fin de lograr un nivel de seguridad razonable con cualquiera de las tecnologías Microsoft descritas en esta guía. La configuración del sistema que se muestra en la interfaz de usuario como **Solicitar una contraseña cuando el equipo se active tras un tiempo de inactividad** se puede configurar bien mediante Directivas de grupo o bien ejecutando scripts que ajusten la configuración del Registro.

#### Adición de seguridad en entornos de poca amenaza

Algunas organizaciones cuentan con requisitos de seguridad relativamente modestos, pero siguen deseando la protección adicional de saber que los datos de sus equipos móviles están cifrados. Para estas organizaciones, BitLocker con un TPM y NIP proporciona una gran seguridad con mínimos costos generales de operaciones (aparte del requisito de asegurar que los usuarios autorizados pueden recuperar los datos protegidos). Si la organización no puede implementar BitLocker, EFS minimiza la amenaza del acceso a datos por parte de usuarios no autorizados tanto en Microsoft Windows® XP como en Windows Vista™. La ejecución de EFS en Windows Vista también ayuda a minimizar el riesgo de pérdida de datos del archivo de paginación del sistema. Sin embargo, seguirá necesitando minimizaciones adicionales para protegerse frente a otros ataques, incluidos los ataques sin conexión contra el sistema operativo y los intentos de robo de material de claves.

#### Protección de información de identificación personal

Si la organización necesita proteger la información de identificación personal (PII) que se encuentra en los portátiles de los empleados frente a amenazas externas y la evaluación de riesgos indica que la protección frente a ataques de dificultad media es adecuada, puede elegir implementar BitLocker con un TPM y NIP. Con esta solución, el principal riesgo planteado por intrusos que necesita minimización adicional se produce cuando un equipo se deja desprotegido en modo de suspensión o en espera. Este riesgo se puede minimizar mediante Directivas de grupo o scripts que ajusten la configuración del Registro.

Para entornos en los que necesite proteger la información PII, pero no pueda usar BitLocker con un TPM, deberá considerar la implementación de EFS junto con la herramienta Asistente del sistema de archivos de cifrado de Microsoft (Asistente de EFS). Esta opción ofrece protección frente a un número de ataques de dificultad baja. Para obtener seguridad adicional puede requerir el uso de EFS con tarjetas inteligentes para agregar un factor de autenticación.

Sin embargo, cuando implemente EFS con almacenamiento de claves de software, recuerde que la seguridad de los datos protegidos por EFS depende de la capacidad de un usuario para iniciar sesión. Las contraseñas de inicio de sesión no seguras, las cuentas de equipos compartidos u otras vulnerabilidades de seguridad pueden reducir la seguridad de la implementación de EFS. Estas vulnerabilidades se deberán minimizar junto con la implementación de EFS.

#### Protección de datos extremadamente confidenciales

La solución que combina BitLocker y EFS ofrece protección frente a ataques moderadamente difíciles o muy difíciles en organizaciones que requieren la mayor protección de seguridad frente a usuarios no autorizados y ante intrusos. Por ejemplo, si la organización tiene limitaciones o requisitos concretos para el tamaño del espacio de claves, puede combinar la longitud de clave ajustable de EFS con las capacidades de cifrado del volumen completo de BitLocker para minimizar de forma eficaz una amplia gama de amenazas.

[](#mainsection)[Principio de la página](#mainsection)

### Conclusión

Las dos tecnologías descritas en esta guía, BitLocker y EFS, representan enfoques del cifrado de datos que son al mismo tiempo diferentes y complementarios. EFS protege los datos residentes en archivos y carpetas por usuario, mientras que BitLocker proporciona un cifrado completo del volumen del sistema en equipos Windows Vista. BitLocker proporciona comprobación y cifrado de la integridad anterior al inicio y protege el volumen del sistema frente a una amplia gama de ataques sin conexión, pero no proporciona autenticación de usuario. EFS complementa a BitLocker al limitar el acceso a archivos cifrados a los usuarios autenticados correctamente en un equipo en ejecución.

Esta guía de *Análisis de seguridad* describe cómo se pueden usar BitLocker y EFS para minimizar el intervalo de riesgos de seguridad. Mediante una evaluación exhaustiva de los riesgos reales de la organización y las minimizaciones descritas en esta guía, podrá elegir una combinación de tecnologías y opciones que proporcionen la protección necesaria para sus datos confidenciales.

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Obtener Data Encryption Toolkit for Mobile PCs](http://go.microsoft.com/fwlink/?linkid=81666)

**Participar**

[Suscríbase para participar en el programa beta de Data Encryption Toolkit](https://connect.microsoft.com/invitationuse.aspx?programid=790&invitationid=desa-r7gd-3f73&siteid=14)

**Notificaciones de actualizaciones**

[Suscríbase para obtener información acerca de las actualizaciones y las nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)

**Comentarios**

[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=data%20encryption%20toolkit%20for%20mobile%20pcs%20security%20analysis%20on%20technet)

[](#mainsection)[Principio de la página](#mainsection)
