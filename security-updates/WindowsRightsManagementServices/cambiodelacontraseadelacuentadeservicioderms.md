---
TOCTitle: Cambio de la contraseña de la cuenta de servicio de RMS
Title: Cambio de la contraseña de la cuenta de servicio de RMS
ms:assetid: '435c9cef-b622-48b3-9d4d-4bf5cac7d52d'
ms:contentKeyID: 18127792
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720273(v=WS.10)'
---

Cambio de la contraseña de la cuenta de servicio de RMS
=======================================================

Según la directiva de contraseñas que especifique para los servidores de RMS, es posible que la contraseña de la cuenta de servicio de RMS caduque periódicamente. Si la contraseña caduca, RMS dejará de funcionar. Por tanto, es vital que cambie la contraseña antes de que caduque.

**Uso de una cuenta de servicio de RMS**

Cuando se utiliza una sola cuenta de servicio de RMS, puede cambiar la contraseña de cada servidor de RMS como se indica a continuación:

1.  Si el servidor se encuentra en un clúster, excluya el servidor de la rotación.
2.  Inicie sesión en el servidor con las credenciales de la cuenta de servicio de RMS.
3.  Cambie la contraseña de la cuenta de servicio de RMS.
    Los demás servidores que utilicen la misma cuenta de servicio de RMS quedarán fuera de servicio, porque las credenciales que se almacenan en ellos quedarán invalidadas cuando se cambie la contraseña.
4.  Cierre sesión en el servidor.
5.  Vuelva a iniciar sesión en el servidor utilizando las credenciales de administrador de RMS.
6.  Para configurar de nuevo la identidad de usuario en el servidor, en la página **Administración global**, haga clic en **Cambiar la cuenta de servicio de RMS** y, a continuación, en la página **Cambiar la cuenta de servicio de RMS**, especifique el dominio, el nombre de usuario y la contraseña.
7.  Reinicie IIS.
8.  Si procede, vuelva a incluir el servidor en la rotación.
9.  Repita los pasos 6 a 8 para todos los servidores que formen parte del clúster.

Éste es el método más sencillo para cambiar la contraseña de la cuenta de servicio de RMS; sin embargo, puede producirse un cierto tiempo de inactividad de Windows RMS, ya que cuando cambia la contraseña de cuenta de servicio RMS de un servidor, Active Directory se actualiza con la nueva contraseña. IIS reinicia periódicamente los grupos de aplicaciones y aquellos que se ejecuten utilizando las antiguas credenciales no podrán iniciarse hasta que cambie la contraseña de la cuenta de servicio de RMS y reinicie IIS en ese servidor. RMS no puede funcionar hasta que los grupos de aplicaciones vuelvan a ser operativos.

**Uso de dos cuentas de servicio de RMS**

Con este método, cree primero dos cuentas de servicio de RMS con diferentes directivas o fechas de caducidad. Durante el funcionamiento normal, RMS se ejecuta con la primera cuenta. Cuando esté preparado para cambiar la contraseña de la primera cuenta de servicio, realice este procedimiento en todos los servidores de RMS:

1.  Si el servidor se encuentra en un clúster, excluya el servidor de la rotación.
2.  Especifique la segunda cuenta de servicio de RMS como la cuenta con la que se ejecutará RMS. Para obtener instrucciones sobre cómo cambiar la cuenta, vea "[Cambio de la cuenta de servicio de RMS](https://technet.microsoft.com/f257d66d-b823-41e4-bcb7-7c90eb295238)", más adelante en este tema.
3.  Reinicie IIS.
4.  Si procede, vuelva a incluir el servidor en la rotación.

Cuando todos los servidores de RMS utilicen la segunda cuenta de servicio de RMS, podrá cambiar la contraseña de la primera cuenta de servicio de RMS sin que el funcionamiento del sistema RMS se vea afectado. Puede alternar entre ambas cuentas de esta manera y evitar así el tiempo de inactividad de RMS.
