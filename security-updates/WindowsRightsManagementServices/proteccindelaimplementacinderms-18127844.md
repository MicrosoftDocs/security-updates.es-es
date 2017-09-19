---
TOCTitle: Protección de la implementación de RMS
Title: Protección de la implementación de RMS
ms:assetid: '6de8b636-a824-4844-aefc-f26347abfc14'
ms:contentKeyID: 18127844
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720291(v=WS.10)'
---

Protección de la implementación de RMS
======================================

Una implementación de RMS es un activo para cualquier organización que requiera las mismas medidas de seguridad física y de red que otros servidores vitales de la infraestructura. Como parte de la implementación, conviene identificar las amenazas y contramedidas que afectan a los servidores RMS.

RMS se implementa como servicio Web, de modo que puede controlar el acceso a RMS de la misma forma que lo haría con otros servicios Web, utilizando listas de control de acceso y capa de sockets seguros.

**Restricción del acceso a servicios Web de RMS mediante ACL**

Se puede restringir el acceso a los servicios de RMS mediante listas de control de acceso (ACL). Cada una de las raíces virtuales que se crean al establecer los servicios en línea de RMS en un sitio Web tiene una estructura de carpetas correspondiente que se puede proteger. La estructura de carpetas se encuentra en &lt;unidad del sistema&gt;:\\&lt;*carpeta\_raíz\_web*&gt;\\\_wmcs, donde *carpeta\_raíz\_web* es el nombre de la carpeta asignada al sitio Web en el que se establecen los servicios en línea de RMS. Algunos de los servicios Web, como el servicio de subinscripción, el servicio de certificación de dispositivos móviles y el servicio de certificación de servicio de servidor, están restringidos de forma predeterminada, y es preciso agregar explícitamente a la lista de control de acceso a los usuarios o grupos que desee que puedan utilizar el servicio.

El servicio de certificación de servicio de servidor proporciona certificados de cuenta de permisos (RAC) que pueden utilizarse para acceder a servicios protegidos con RMS como servicios de colaboración Web, servidores de correo y servidores de administración de documentos para permitir la extensión de un sistema RMS, como:

-   Un servidor de colaboración de documentos donde los usuarios pueden cargar documentos desprotegidos. Sin embargo, a los documentos descargados se les aplicará automáticamente la protección con RMS de acuerdo con la directiva de permisos para el tipo de contenido. Un ejemplo es Microsoft Office SharePoint Server 2007.
-   Un sistema de administración de documentos que sirva como repositorio general y archivo de documentos, tanto protegidos como desprotegidos. El sistema podrá indizar documentos protegidos con derechos para su búsqueda conservando la directiva de permisos definida por el creador de contenido.
-   Habilite el servidor de correo para que abra rápidamente el contenido protegido con derechos a fin de analizar posibles virus, correo electrónico no deseado o como parte de un requisito legal o de la política de correo de la empresa.

Dado que estos escenarios requieren licencias en nombre de sus usuarios, puede requerir que la capacidad de los servidores para obtener RAC esté limitada exclusivamente a los servidores de su organización que hayan sido aprobados para dicha función y que tengan la protección adecuada.

**Restricción del acceso a servicios Web de RMS mediante SSL**

Es recomendable que habilite la capa de sockets seguros (SSL) y que requiera el cifrado de 128 bits en cada uno de los archivos de los servicios Web de RMS. Estos archivos tienen la extensión de nombre de archivo .asmx y se encuentran en los directorios virtuales Licensing, Certification y Admin. SSL requiere que el servidor tenga un certificado SSL válido instalado para el sitio Web. Si aplica SSL a la carpeta \_wmcs de la instalación de RMS, las subcarpetas y los archivos heredarán la configuración. Para obtener más información sobre los archivos de los servicios Web y los directorios virtuales, consulte "Servicios de Internet Information Server" en la sección "RMS: referencia técnica" en esta recopilación de documentación.

| ![](images/Cc720291.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Si desea abrir las páginas Web de administración de Windows RMS en un explorador ubicado en un equipo remoto, debe habilitar SSL. Sin embargo, incluso con SSL habilitada, no puede abrir la página **Administración global** desde un equipo remoto. Para obtener más información sobre la administración remota de RMS, consulte "Uso de la página principal de administración" en la sección "RMS: operaciones" en esta recopilación de documentación. |

**Configuración de una contraseña de clave privada segura**

La contraseña de clave privada se utiliza para generar y almacenar de forma segura la clave privada en la base de datos de configuración de RMS. Se recomienda una contraseña segura para garantizar la máxima seguridad. Si es necesario escribir la contraseña, asegúrese de almacenar esta contraseña en un área físicamente segura.

| ![](images/Cc720291.Caution(WS.10).gif)Precaución                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Si la contraseña de clave privada se pierde o se desconoce, y el servidor RMS se desconecta inesperadamente, deberá descifrar todos los documentos RMS, reconstruir el entorno RMS y cifrarlo todo de nuevo con la nueva clave privada. |
