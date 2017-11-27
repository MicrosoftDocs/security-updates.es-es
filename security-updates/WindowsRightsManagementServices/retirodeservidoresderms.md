---
TOCTitle: Retiro de servidores de RMS
Title: Retiro de servidores de RMS
ms:assetid: '11badb02-62c1-455c-96b7-935bbcb496bc'
ms:contentKeyID: 18127729
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720200(v=WS.10)'
---

Retiro de servidores de RMS
===========================

Cuando se retira RMS, el funcionamiento del servidor de RMS cambia de forma que podrá proporcionar una clave que descifre el contenido protegido con RMS publicado anteriormente. Esta clave permite que el contenido se guarde sin protección de RMS. Esto puede resultar útil si ha decidido dejar de utilizar la protección de RMS en su organización.

Debe ejecutar el servidor en estado de retiro durante el tiempo suficiente para que los usuarios puedan guardar su contenido sin protección de RMS y para que los administradores de la red y del sistema puedan deshabilitar el servicio para los clientes compatibles con RMS.

Puede habilitar el retiro en la página Web **Configuración de seguridad** del sitio Web de administración. Después de habilitar el retiro, no podrá restablecer una configuración de servidor de RMS estándar en el servidor. Si la instalación incluía dominios de publicación de confianza, éstos se retiran también.

Una vez habilitado el retiro, el sitio Web de administración sólo contiene la página **Información del servidor retirado**; no se admite ninguna otra función administrativa. Debe llevar a cabo los siguientes pasos para completar el retiro del servidor:

1.  Conceda a la raíz virtual que se va a retirar los permisos de lectura y ejecución de **RMS Service Group**.

2.  Agregue el grupo **Todos** a la lista DACL del archivo decommissioning.asmx con permisos de lectura.

3.  Informe a los usuarios de que va a retirar la instalación de RMS y aconséjeles que se conecten al servidor para guardar su contenido sin protección de RMS.

4.  Configure todas las aplicaciones compatibles con RMS de la empresa para que se conecten a la página decommissioning.asmx. Según la aplicación compatible con RMS, esto se puede controlar mediante una clave de registro o la configuración de directiva de grupo.

5.  Si la organización utiliza aplicaciones compatibles con RMS que usen automáticamente la instalación para publicar, debe utilizar la directiva de grupo para establecer una entrada de registro en estos equipos para que dichas aplicaciones empleen el servicio de retiro.

6.  Cuando crea que se ha desprotegido todo el contenido, realice una copia de seguridad de la clave privada del servidor y, a continuación, desinstale RMS del servidor.