---
TOCTitle: Dominios de publicación de confianza
Title: Dominios de publicación de confianza
ms:assetid: 'bca1c33a-d3ef-42b5-adbe-6e104979a71f'
ms:contentKeyID: 18127926
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747738(v=WS.10)'
---

Dominios de publicación de confianza
====================================

De forma predeterminada, los servidores de RMS no emiten licencias de uso para las licencias de publicación que hayan sido emitidas por un servidor de RMS de un clúster distinto. Sin embargo, hay situaciones en que el mismo servidor o clúster no puede emitir licencias de uso y de publicación para un fragmento de contenido protegido. Por ejemplo, esto puede ocurrir si un clúster de RMS determinado se retira y otro toma su lugar, como cuando dos compañías se fusionan. En esta situación, un clúster de RMS debe poder emitir licencias de uso para las licencias de publicación creadas por un clúster de RMS distinto.

Si se implementa un dominio de publicación de confianza, se puede configurar un clúster de RMS para que considere de confianza las licencias de publicación emitidas por otro clúster de RMS y que emita licencias de uso para ellas. Esto se logra importando del otro servidor el certificado emisor de licencias de servidor y la clave privada, y agregándolo, a continuación, a la lista de dominios de publicación de confianza. Las claves privadas que se importan se usan sólo para descifrar licencias de publicación firmadas, y no para firmar nuevas licencias.

Para obtener más información acerca de los dominios de usuarios de confianza e instrucciones paso a paso, vea "Adición y desinstalación de dominios de publicación de confianza" y "Establecimiento de directivas de confianza" en "Operación de un servidor de RMS", en esta recopilación de documentación.
