---
TOCTitle: Exclusión de aplicaciones
Title: Exclusión de aplicaciones
ms:assetid: 'b68ae4b2-b9ba-44ae-90cb-c88df600ec86'
ms:contentKeyID: 18127924
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747644(v=WS.10)'
---

Exclusión de aplicaciones
=========================

Puede especificar la versión de una aplicación compatible con RMS para que se utilice para comprobar todas las solicitudes de licencias. La exclusión de aplicaciones marca todas las licencias de uso con una condición por la que la licencia sólo puede enlazarse al contenido protegido con RMS para el que se haya emitido, si la aplicación que solicita la licencia no se encuentra en la lista de exclusión.

Esto puede resultar útil, por ejemplo, cuando una empresa implementa una actualización de seguridad de una aplicación. Los administradores del sistema pueden utilizar este mecanismo para hacer que los equipos cliente instalen la actualización de seguridad. A continuación, pueden establecer directivas de exclusión de aplicaciones que se definan utilizando la información de versión de la aplicación que utiliza el sitio Web de administración. Esta directiva de exclusión impide a RMS emitir licencias a clientes que utilicen versiones anteriores del software.

Las aplicaciones compatibles con RMS se excluyen en función del nombre de archivo y el número de versión. Es posible que desee crear esta exclusión para asegurarse de que los usuarios instalen una versión más reciente y segura de una aplicación cuando esté disponible. Por ejemplo, puede tener la versión 1.0.4.2315 de una aplicación compatible con RMS que se ha implementado en su organización. Después, el programador de la aplicación descubre un problema de seguridad y emite la versión 1.0.4.4200, que elimina dicho problema. Además de realizar la implementación de la nueva versión de la aplicación, puede establecer una directiva de exclusión que impida que los usuarios utilicen contenido protegido si usan la versión anterior de la aplicación.

Al igual que con otros tipos de exclusión, debe configurar la exclusión de aplicaciones en cada clúster en el que desea que surta efecto.

Cuando aplique esta directiva de exclusión en el servidor, los clientes no podrán usar la aplicación excluida para solicitar y enlazar nuevas licencias de uso a contenido protegido con RMS. No obstante, los clientes pueden continuar utilizando la aplicación excluida para utilizar archivos con una licencia anterior.

| ![](images/Cc747644.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RMS requiere que se especifique la versión de la aplicación en un formato de 4 dígitos separados por puntos (\#.\#.\#.\# ). Sin embargo, algunas aplicaciones especifican la versión de la aplicación en un formato de 2 o 3 dígitos separados por puntos. En este caso, deberá agregar tantas veces como convenga .0 para que el número de versión coincida con el formato requerido por RMS. |
