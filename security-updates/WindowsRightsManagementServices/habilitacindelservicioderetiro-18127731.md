---
TOCTitle: Habilitación del servicio de retiro
Title: Habilitación del servicio de retiro
ms:assetid: '45226e85-b50d-41cc-aca7-0f603f8509d5'
ms:contentKeyID: 18127731
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720261(v=WS.10)'
---

Habilitación del servicio de retiro
===================================

Para retirar el sistema RMS es necesario utilizar la clave privada para proteger toda la información publicada. Esta clave privada se almacena en la base de datos de configuración, cifrada por una API de protección de datos (DPAPI), y se basa en la contraseña que se introdujo durante el establecimiento. Si la clave privada de RMS se almacena en un módulo de seguridad de hardware (HSM), la clave privada se almacena en el HSM en lugar de en la base de datos de configuración.

| ![](images/Cc720261.Caution(WS.10).gif)Precaución                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Antes de retirar el sistema RMS, asegúrese de conocer la contraseña de clave privada. Si no la conoce, debe restablecer la contraseña de clave privada antes de retirar el servidor RMS. |

El primer paso para quitar el sistema RMS es retirar los servidores del clúster. Puesto que el retiro es una función de la licencia, un servidor en un clúster de sólo licencias de RMS subinscrito se puede retirar sin que afecte al clúster raíz de RMS ni a ningún otro clúster de sólo licencias de RMS subinscrito. Por lo tanto, es necesario retirar por separado el clúster raíz de RMS y los clústeres de sólo licencias, ya que cada clúster de sólo licencias tiene su propia clave privada, que se utiliza para crear licencias de publicación.

Utilice el procedimiento siguiente para habilitar el servicio de retiro:

1.  Abra el sitio Web de administración de Windows RMS.
2.  Haga clic en **Administrar RMS** y, a continuación, haga clic en **Configuración de seguridad**.
3.  Seleccione la casilla de verificación **Habilitar el retiro de la instalación de RMS**.
4.  Cuando el cuadro de diálogo le pida que confirme el proceso de retiro, haga clic en **Aceptar**.

Cuando se retira un servidor, no es posible restaurar en él una configuración de RMS estándar. Este procedimiento es irreversible.

Una vez retirado, RMS debe quitarse por completo mediante la opción **Agregar o quitar programas** antes de intentar instalar otra instancia de RMS.
