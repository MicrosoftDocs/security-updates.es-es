---
TOCTitle: Definición de los requisitos de administración de claves
Title: Definición de los requisitos de administración de claves
ms:assetid: 'f0e08fb8-bf5e-4278-a09f-daa57696e786'
ms:contentKeyID: 18128021
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747797(v=WS.10)'
---

Definición de los requisitos de administración de claves
========================================================

RMS utiliza claves de cifrado para proteger contenido y exigir permisos. Las claves de cifrado son datos fundamentales que permiten al sistema funcionar sin problemas y de manera segura. Los administradores deben encargarse de administrar estas claves de forma adecuada para protegerlas de la pérdida de datos, errores del sistema y robo.

En la configuración predeterminada, RMS almacena el par de claves del servidor y el GUID asociado en una tabla que se encuentra en la base de datos de configuración. El par de claves del servidor está cifrado con la contraseña que selecciona durante el proceso de establecimiento de servicios en línea.

Para ayudar a proteger el par de claves de servidor y el GUID asociado, realice una copia de seguridad de la base de datos de configuración en un medio de almacenamiento (como por ejemplo un CD) y, a continuación, guarde el medio de almacenamiento en un lugar seguro (como una caja de seguridad en otro lugar). La programación de copias de seguridad depende de la frecuencia con la que realice cambios administrativos y del nivel de riesgo de pérdida de datos aceptable como consecuencia de la degradación u otros riesgos de los medios. Asegúrese de tener una forma de saber qué contraseña de la clave privada se utiliza con la base de datos de configuración de la que ha realizado una copia de seguridad. Sin la contraseña adecuada no podrá restaurar la copia de seguridad en el servidor de RMS.

Si está utilizando SQL Server como servidor de base de datos, puede utilizar el Administrador corporativo de SQL Server para copiar directamente el valor del GUID y los datos de la clave privada cifrada en un disquete u otro medio seguro. Dado que la clave privada está protegida, la instalación de RMS debe ejecutarse con la misma cuenta de servicio de RMS que la copia de seguridad, si la restaura desde medios seguros en una instalación de RMS.

Si utiliza un CSP de software o de hardware para proteger la clave privada del servidor, debe realizar manualmente una copia de seguridad de la clave y del contenedor de la clave. Si utiliza un módulo de seguridad de hardware, se mejora la seguridad de las claves privadas, ya que se mantienen en hardware y nunca se ven expuestas a software. Los datos que deben firmarse o descifrarse se transfieren al módulo de seguridad de hardware, se descifran o firman y después se vuelven a transferir.

Cada CSP, ya sea de hardware o de software, tiene procedimientos específicos para realizar copias de seguridad de la clave de forma segura; si no está familiarizado con este procedimiento, consulte la documentación del CSP.
