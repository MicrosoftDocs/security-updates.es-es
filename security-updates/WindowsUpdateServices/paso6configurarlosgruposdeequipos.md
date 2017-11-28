---
TOCTitle: 'Paso 6: configurar los grupos de equipos'
Title: 'Paso 6: configurar los grupos de equipos'
ms:assetid: '70518732-2179-4e41-9609-7f9999867f41'
ms:contentKeyID: 21741369
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd939860(v=WS.10)'
---

Paso 6: configurar los grupos de equipos
========================================

Los grupos de equipos son una parte importante de las implementaciones de Windows Server Update Services 3.0 Service Pack 2 (WSUS 3.0 SP2), ya que permiten probar las actualizaciones y dirigirlas a equipos específicos. Hay dos grupos de equipos predeterminados: Todos los equipos y Equipos sin asignar. De forma predeterminada, cuando cada equipo cliente se pone en contacto inicialmente con el servidor WSUS, éste agrega dicho equipo cliente a cada uno de estos grupos.

Puede crear tantos grupos de equipo personalizados como necesite para administrar y ordenar todas las actualizaciones. Si desea llevar a cabo el procedimiento recomendado, cree al menos un grupo de equipos para poder probar las actualizaciones antes de implementarlas en otros equipos de su organización.

Procedimientos del paso 6
-------------------------

1.  Crear un grupo de equipos de prueba.
2.  Mover al menos un equipo a un grupo de prueba.

**Para crear un grupo de prueba**
1.  En la consola de administración de WSUS, expanda **Equipos** y seleccione **Todos los equipos.**

2.  Haga clic con el botón secundario en **Todos los equipos** y haga clic en **Agregar grupo de equipos**.

3.  En el cuadro de diálogo **Agregar grupo de equipos**, especifique el **Nombre** del nuevo grupo de prueba y haga clic en **Agregar**.

Use el procedimiento siguiente para asignar un equipo cliente al grupo de prueba. Un equipo de prueba es cualquier ordenador que posea un software y un hardware coherente con la mayoría de los equipos cliente en la red, pero no asignado a una función crítica. Después de que las pruebas se hayan realizado correctamente, puede aprobar las actualizaciones para los equipos en los grupos que desee.

**Para asignar un equipo al grupo de prueba**
1.  En la consola de administración de WSUS, haga clic en **Equipos**.

2.  Haga clic en el grupo de equipos que desee asignar al grupo de prueba.

3.  En la lista de equipos, seleccione el ordenador o los ordenadores que desee asignar al grupo de prueba.

4.  Haga clic con el botón secundario del mouse en **Cambiar pertenencia**.

5.  En el cuadro de diálogo **Establecer pertenencia a un grupo de equipos**, seleccione el grupo de prueba que haya creado previamente y haga clic en **Aceptar**.

Repita estos dos procedimientos, es decir, cree un grupo y, a continuación, asígnele los ordenadores que desee, para crear tantos grupos de equipos adicionales como necesite para administrar las actualizaciones en su sitio.

Paso siguiente
--------------

[Paso 7: aprobar e implementar las actualizaciones de WSUS](https://technet.microsoft.com/c4e58e17-d5e3-4194-8f26-b459e0c03b86)

Recursos adicionales
--------------------

[Guía paso a paso para Windows Server Update Services 3.0 SP2](https://technet.microsoft.com/4b504edc-93b3-45b0-a7e8-d0107f1a4442)
