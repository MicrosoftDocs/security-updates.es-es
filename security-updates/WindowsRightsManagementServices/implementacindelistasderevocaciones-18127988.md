---
TOCTitle: Implementación de listas de revocaciones
Title: Implementación de listas de revocaciones
ms:assetid: 'e331338b-66d4-45e4-8d3f-acccf2302ac4'
ms:contentKeyID: 18127988
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747702(v=WS.10)'
---

Implementación de listas de revocaciones
========================================

Para implementar la revocación, debe implementar listas de revocaciones. Las listas de revocaciones especifican el contenido, las aplicaciones, los usuarios u otras entidades principales que han sido revocadas. Puede implementar listas de revocaciones tanto de la organización como de Microsoft.

Implementación de listas de revocaciones de la organización
-----------------------------------------------------------

Para utilizar una plantilla de directiva de permisos con una lista de revocaciones, debe poner la lista de revocaciones a disposición de los equipos cliente en la organización. Para obtener más información acerca de la creación de listas de revocaciones, vea “Implementación de revocaciones”, anteriormente en este tema.

Para implementar una lista de revocaciones de la organización, siga estos pasos:

1.  Copie el archivo de lista de revocaciones en un servidor Web accesible públicamente. Puesto que los usuarios pueden utilizar el contenido protegido fuera de la organización, la ubicación especificada debe resultar accesible a todos los usuarios, tanto dentro como fuera de la red.
    La distribución del archivo de lista de revocaciones a los equipos cliente puede tardar cierto tiempo. Esto crea la posibilidad de que los usuarios no tengan acceso a la lista de revocaciones en sus equipos clientes cuando intenten abrir un documento que precisa una lista de revocaciones. Si la lista de revocaciones no se encuentra en el equipo cliente, la aplicación compatible con RMS puede descargarla de la ubicación especificada en la licencia de uso.
    Lo ideal es crear una secuencia de comandos que automáticamente firme y copie la lista de revocaciones en el sitio Web todos los días. Esto ayuda a garantizar que los usuarios no dejen de utilizar contenido porque su lista de revocaciones no está actualizada. Para obtener una secuencia de comandos de muestra, vea “Uso de la herramienta de firma de lista de revocaciones”, anteriormente en este tema.
2.  En la plantilla de directiva de permisos, especifique un intervalo de actualización mayor que cero para la lista de revocaciones de la organización. Esto garantiza que la lista de revocaciones no sea opcional. Si va a actualizar la lista con poca frecuencia, por ejemplo, sólo si se produce una infracción de seguridad, puede establecer la condición de actualización con un intervalo prolongado y después depender de la configuración de directivas o secuencias de comandos para insertar la lista de revocaciones en los equipos cliente cuando sea necesario. Para obtener información acerca del establecimiento de intervalos de actualización, vea “Definición de directivas de revocación”, anteriormente en este tema. Para obtener más información acerca de la configuración de plantillas de directiva de permisos, vea “Creación y modificación de plantillas de directiva de permisos”, más adelante en este tema.
3.  En la plantilla de directiva de permisos, especifique la dirección URL en la que está disponible la lista de revocaciones.
4.  Opcionalmente, implemente la lista de revocaciones en los equipos cliente utilizando un método automatizado, como la directiva de grupo o SMS (Systems Management Server).

Implementación de listas de revocaciones de Microsoft
-----------------------------------------------------

Para que el cliente de los Servicios de Rights Management utilice una lista de revocaciones de Microsoft, debe implementar la lista en los equipos cliente. Este tema explica cómo implementar una lista de revocaciones de Microsoft en los siguientes escenarios:

-   Su organización desea implementar su propia lista de revocaciones y la de Microsoft.
-   Su organización desea implementar únicamente la lista de revocaciones de Microsoft.

Cuando Microsoft publica una lista de revocaciones, se puede descargar de las ubicaciones siguientes:

-   Los servidores de RMS podrán descargar la lista de revocaciones con Windows Update.
-   Como alternativa, la lista de revocaciones de Microsoft también estará disponible para descargarla en Microsoft Download Center si el servidor de RMS no está conectado a Internet.

Si descarga el paquete de lista de revocaciones en un servidor de RMS, se guarda en la carpeta %systemdrive%\\Archivos de programa\\Windows Rights Management Services Revocation List. Si va a descargar el paquete de lista de revocaciones en otro tipo de equipo, puede seleccionar la ubicación de descarga. El paquete contiene un archivo ejecutable, CRL\_Update.exe, que se puede ejecutar para instalar todas las listas de revocaciones de cliente en el almacén de licencias de cliente y también un archivo de lista de revocaciones, Msrl.xml, que se puede copiar en un sitio Web o en una carpeta compartida pública.

**Para implementar las listas de revocaciones de su organización y de Microsoft**
1.  Para implementar la lista de revocaciones de su organización, siga las instrucciones de “[Implementación de listas de revocaciones](https://technet.microsoft.com/e331338b-66d4-45e4-8d3f-acccf2302ac4)”, anteriormente en este tema.

2.  Descargue el paquete de lista de revocaciones de Microsoft e impleméntelo en todos los equipos cliente de la organización utilizando la directiva de grupo o SMS (Systems Management Server). Como alternativa, puede copiar entradas de la lista de revocaciones de Microsoft en la de la organización e implementar sólo esta última.

| ![](images/Cc747702.Caution(WS.10).gif)Precaución                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft es una entidad principal de la cadena de confianza de todos los certificados y licencias que RMS emite. Por tanto, una lista de revocaciones emitida por Microsoft es efectiva para todas las solicitudes de enlace para las que se obtenga la licencia de uso en función de una plantilla de directiva de permisos que precise la lista de revocaciones de la organización. Además, la lista de revocaciones de Microsoft se registra en el equipo cliente. |

**Para implementar únicamente una lista de revocaciones de Microsoft**
1.  Descargue el paquete de lista de revocaciones de Microsoft.

2.  Modifique las plantillas de directiva de permisos existentes para que requieran la revocación o, si no existe ninguna, cree una que requiera revocación. Utilice la clave pública de Microsoft cuando especifique la condición de revocación.

3.  Utilice un intervalo de actualización muy elevado, como 50.000. Este elevado número garantiza que la lista de revocaciones que Microsoft publique no caduque nunca. Por tanto, las licencias de uso que distribuya no necesitarán una nueva versión de la lista de revocaciones de Microsoft cuando es posible que no haya una disponible.

4.  Copie el archivo de lista de revocaciones en un servidor Web accesible públicamente. Puesto que los usuarios pueden utilizar el contenido protegido fuera de la organización, la ubicación especificada debe resultar accesible a todos los usuarios, tanto dentro como fuera de la red.

5.  Debe hacer que la lista de revocaciones esté disponible, puesto que la distribución del archivo de lista de revocaciones a los equipos cliente puede tardar bastante tiempo. Por esta razón, es posible que un usuario no tenga acceso a la lista de revocaciones localmente en su equipo cuando intente abrir un documento con una licencia de publicación que precise revocación. Si la lista de revocaciones no está presente en el equipo cliente, la aplicación compatible con RMS puede descargarla de la ubicación especificada.

6.  En la plantilla de directiva de permisos, especifique la dirección URL en la que está disponible la lista de revocaciones. Para obtener más información acerca de la configuración de plantillas de directiva de permisos, vea “[Creación y modificación de plantillas de directiva de permisos](https://technet.microsoft.com/6014176f-ef71-4d29-b3e3-da129c18563d)”, más adelante en este tema.

7.  Opcionalmente, implemente el paquete de lista de revocaciones en los equipos cliente utilizando un método como directivas de grupo o SMS. A continuación, los usuarios pueden abrir contenido protegido con RMS que precise listas de revocaciones, incluso cuando no estén conectados a la red.
