---
TOCTitle: Configuración de dispositivos de cifrado de hardware
Title: Configuración de dispositivos de cifrado de hardware
ms:assetid: '3a35a8ea-696c-4005-9892-cac6e773497a'
ms:contentKeyID: 18127785
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720248(v=WS.10)'
---

Configuración de dispositivos de cifrado de hardware
====================================================

RMS puede utilizar los proveedores de servicios de cifrado (CSP) estándar de Windows, como los CSP básicos y mejorados, para generar las claves públicas y privadas que se almacenarán en la base de datos de configuración y se utilizarán para proteger el contenido. Se recomienda que estas claves tengan aplicada protección adicional, porque se almacenan en software. Para proporcionar protección de claves de nivel superior, se puede utilizar un CSP de hardware proporcionado por un módulo de seguridad de hardware (HSM).

Si va a utilizar un HSM para proporcionar seguridad adicional para sus claves de servidor, instale y configure el hardware en los servidores antes de empezar la instalación de RMS.
