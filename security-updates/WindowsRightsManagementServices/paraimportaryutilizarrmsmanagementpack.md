---
TOCTitle: Para importar y utilizar RMS Management Pack
Title: Para importar y utilizar RMS Management Pack
ms:assetid: 'd9a73ef0-2f81-48c2-97cc-deb7bf477389'
ms:contentKeyID: 18127983
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747688(v=WS.10)'
---

Para importar y utilizar RMS Management Pack
============================================

Importación y uso de RMS Management Pack
----------------------------------------

#### Para importar y utilizar RMS Management Pack

1.  Copie RMS Management Pack (RMS\_MOMPack.akm) de la carpeta %ProgramFiles%\\Windows Rights Management Services\\Tools en el servidor de Microsoft Operations Manager (MOM).

2.  Abra la consola de administrador de MOM y, a continuación, importe RMS Management Pack siguiendo estos pasos:

    1.  En el árbol de la consola de administrador de MOM, expanda el elemento **Rules** y, a continuación, haga clic con el botón secundario del mouse en el elemento **Processing Rule Groups**.
    2.  En el menú contextual, haga clic en **Importar paquete de administración**. Se mostrará el cuadro de diálogo **Import Management Pack**.
    3.  Haga clic en **Browse** y, a continuación, seleccione RMS\_MOMPack.akm.

3.  Especifique las opciones de combinación o reemplazo. Para obtener más información acerca de las opciones de combinación y reemplazo, vea "Exporting and Importing Management Packs" (Exportación e importación de paquetes de administración) en el sitio Web de Microsoft (http://www.microsoft.com/).

    Haga clic en **Replace**. La opción de reemplazo hace que el paquete de administración importado sobrescriba los grupos de reglas de procesamiento existentes, no se conserva ningún comentario de usuario. Si desea combinar este paquete de administración con un paquete de administración existente, debe hacerlo en un entorno de prueba y, a continuación, utilizar la opción **Replace** cuando implemente el paquete de administración en el entorno de producción.

4.  Haga clic en **Import** para importar el paquete de administración.

5.  En la consola de **administrador de MOM**, seleccione el elemento **Configuration** y, a continuación haga clic en la carpeta **Agent Managers**.

6.  Haga clic con el botón secundario del mouse en el servidor en el que haya importado RMS Management Pack y, a continuación, haga clic en **Scan Managed Computers Now**.
