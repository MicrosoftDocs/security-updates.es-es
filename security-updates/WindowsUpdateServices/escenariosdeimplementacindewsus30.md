---
TOCTitle: 'Escenarios de implementación de WSUS 3.0'
Title: 'Escenarios de implementación de WSUS 3.0'
ms:assetid: '18a4a8d4-d002-46b1-98db-74a0aed42ddf'
ms:contentKeyID: 18158184
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720467(v=WS.10)'
---

Escenarios de implementación de WSUS 3.0
========================================

### Escenarios de implementación de WSUS 3.0

Publicado: septiembre 11, 2007

WSUS es lo bastante flexible como para satisfacer las necesidades de administración de actualizaciones de una gran variedad de organizaciones, desde la pequeña empresa con conectividad de acceso telefónico hasta las empresas más grandes con miles de usuarios distribuidos entre múltiples lugares. En función del tamaño de la organización, de su ubicación y de su infraestructura de conectividad, los administradores pueden determinar la manera más eficaz de escalar horizontalmente sus servidores WSUS, una decisión ésta que puede implicar a un servidor WSUS, o a varios.

En esta sección obtendrá más información acerca de los escenarios típicos para llevar a cabo la implementación de componentes de WSUS en redes pequeñas, medianas y restringidas.

##### En esta página

[](#ecaa)[Un solo servidor WSUS (red pequeña o sencilla)](#ecaa)  
[](#ebaa)[Varios servidores WSUS (red mediana o más compleja)](#ebaa)  
[](#eaaa)[Servidores WSUS desconectados (conectividad a Internet limitada o restringida)](#eaaa)

### Un solo servidor WSUS (red pequeña o sencilla)

En un escenario con un solo servidor WSUS, los administradores pueden configurar un servidor que ejecute WSUS dentro de su firewall corporativo, el cual sincroniza el contenido directamente con Microsoft Update y distribuye las actualizaciones entre los equipos cliente, tal y como se muestra en la figura siguiente.

![](images/Cc720467.wsus_deploy_01(es-es,WS.10).gif)

Un solo servidor WSUS

[](#mainsection)[Principio de la página](#mainsection)

### Varios servidores WSUS (red mediana o más compleja)

A continuación se muestran escenarios típicos para la implementación de componentes de WSUS en redes medianas o más complejas.

#### Varios servidores WSUS independientes

Los administradores pueden implementar varios servidores configurados de forma que cada uno sea administrado independientemente y sincronice su contenido desde Microsoft Update, tal como se muestra en la figura siguiente.

![](images/Cc720467.wsus_deploy_02(es-es,WS.10).gif)

Varios servidores WSUS independientes

El método de implementación en este escenario sería apropiado en situaciones en las que los diferentes segmentos de redes de área local (LAN) o redes de área extensa (WAN) se administran como entidades separadas (por ejemplo, sucursales). También sería adecuada cuando un servidor que ejecuta WSUS se ha configurado para implementar actualizaciones sólo en equipos cliente que ejecutan un sistema operativo determinado (como, por ejemplo, Windows 2000), mientras otro servidor se ha configurado para implementar actualizaciones sólo en equipos cliente que ejecutan otros sistemas operativos (como, por ejemplo, Windows XP).

#### Varios servidores WSUS sincronizados internamente

Los administradores pueden implementar varios servidores que ejecuten WSUS y que sincronicen todo el contenido de la intranet de la organización. En la figura siguiente sólo hay un servidor expuesto a Internet. En esta configuración, éste es el único servidor que descarga actualizaciones desde Microsoft Update. Este servidor está establecido como el servidor que precede en la cadena, con cuyo origen se sincroniza el servidor que sigue en la cadena. Si es necesario, los servidores pueden ubicarse a través de una red geográficamente dispersa para ofrecer la mejor conectividad posible a todos los equipos cliente.

![](images/Cc720467.wsus_deploy_03(es-es,WS.10).gif)

Varios servidores WSUS sincronizados internamente

[](#mainsection)[Principio de la página](#mainsection)

### Servidores WSUS desconectados (conectividad a Internet limitada o restringida)

Si la directiva corporativa u otras condiciones limitan el acceso del equipo a Internet, los administradores pueden configurar un servidor interno que ejecute WSUS, tal como se muestra en la figura siguiente. En este ejemplo se creó un servidor para conectarlo a Internet; sin embargo, éste se encuentra aislado de la intranet. Después que descargar, probar y aprobar las actualizaciones en este servidor, un administrador podría, a continuación, exportar los metadatos y contenido de las actualizaciones a los medios apropiados. Luego, desde estos medios, el administrador importaría los metadatos y contenido de las actualizaciones en los servidores que ejecutan WSUS dentro de la intranet. Aunque la figura siguiente muestra este modelo en su forma más sencilla, éste podría escalarse a una implementación de cualquier tamaño.

![](images/Cc720467.wsus_deploy_04(es-es,WS.10).gif)

Servidores WSUS desconectados y sin conectividad de la intranet a Internet

[](#mainsection)[Principio de la página](#mainsection)
