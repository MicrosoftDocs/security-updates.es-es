---
TOCTitle: Certificados y licencias de RMS
Title: Certificados y licencias de RMS
ms:assetid: '91916ecb-9e5d-49e8-ab65-ef2c56339b83'
ms:contentKeyID: 18127949
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747600(v=WS.10)'
---

Certificados y licencias de RMS
===============================

Los diferentes componentes de una instalación de RMS tienen conexiones de confianza que se implementan mediante una serie de certificados. Imponer la validez de estos certificados es una función principal de la tecnología de RMS. Todos los fragmentos de contenido protegido con RMS se publican con una licencia que expresa sus reglas de uso, y todos los usuarios de ese contenido reciben una licencia única que lee, interpreta e impone dichas reglas de uso. En este contexto, una licencia es un tipo particular de certificado.

RMS utiliza un vocabulario XML para expresar permisos de uso del contenido protegido con RMS, el lenguaje de marcado de permisos extensible (XrML), versión 1.2.1. Para obtener más información, vea “XrML”, más adelante en este tema.

Los certificados y las licencias de RMS están relacionados mediante una jerarquía, de forma que RMS pueda siempre seguir una cadena que comienza en una licencia o un certificado determinado, pasar por los certificados de confianza y finalizar en un par de claves de confianza. Para obtener más información, vea "[Jerarquía de confianza de RMS](https://technet.microsoft.com/2d44182f-a653-4383-aba1-dade53f7cf9a)", más adelante en este tema.

Se tratan los siguientes temas:

-   [Resumen de certificados y licencias de RMS](https://technet.microsoft.com/637ccfca-318e-4346-85b5-0945b058fb9c)
-   [Certificados emisores de licencias de servidor](https://technet.microsoft.com/0b35fbcd-25a9-4587-898d-9a30fd1d3c5b)
-   [Certificados emisores de licencias de cliente](https://technet.microsoft.com/bfb36387-3e15-4cde-8b8f-482219569a64)
-   [Certificados de equipo de RMS](https://technet.microsoft.com/1841d53e-d01b-47c3-9d43-3805ceefed5a)
-   [Certificados de cuenta de permisos](https://technet.microsoft.com/2ff315cc-211d-4e6e-85e8-56867c2abd94)
-   [Licencias de publicación](https://technet.microsoft.com/187228fc-370b-4e23-a53a-21bb296b84a1)
-   [Licencias de uso](https://technet.microsoft.com/6e609db3-49b3-4cac-a34c-8a96da627067)
