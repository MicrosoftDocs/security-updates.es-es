---
TOCTitle: Retiro de RMS
Title: Retiro de RMS
ms:assetid: 'dbcacce7-434d-48a7-a11d-ef9690d78b44'
ms:contentKeyID: 18127997
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747767(v=WS.10)'
---

Retiro de RMS
=============

La función de retiro se refiere a todo el proceso de eliminar de una organización el servidor de RMS y las bases de datos asociadas. Este proceso le permite eliminar RMS de su infraestructura sin perder acceso a información protegida con RMS. A continuación se enumeran las razones por las que una organización puede querer eliminar un servidor de RMS de su infraestructura:

-   Migración de una prueba de concepto de servidor de RMS desde un entorno piloto al entorno de producción.
-   Simplificación del diseño de arquitectura, eliminando y consolidando servidores de licencias en el clúster raíz de RMS.
-   Fusión de servidores de RMS (por ejemplo, como resultado de una fusión o adquisición empresarial) debido a la integración de dos infraestructuras de RMS en una.
-   Decisión de dejar de utilizar RMS para proteger contenido.

Dado que hay un servidor de RMS activo integrado en los servidores de base de datos y de Active Directory y que, por supuesto, esto protege buena parte del contenido a través de una clave contenida en el servidor de RMS, eliminar RMS de la organización requiere más pasos que simplemente quitar el programa del servidor. En esta sección se indican estos pasos para que pueda retirar el servidor de RMS, si es necesario.

Se tratan los siguientes temas:

-   [Proceso de retiro](https://technet.microsoft.com/57bd9949-9433-437b-93ed-ffb2dff9992e)
-   [Habilitación del servicio de retiro](https://technet.microsoft.com/45226e85-b50d-41cc-aca7-0f603f8509d5)
-   [Establecimiento de permisos de directorio virtual](https://technet.microsoft.com/45112111-9608-45b1-9a86-7b313d0a1579)
-   [Supresión de la protección de RMS del contenido](https://technet.microsoft.com/c30361e3-50d2-4474-a87d-d38de502cf9e)
-   [Supresión del servicio Web (Anulación de RMS)](https://technet.microsoft.com/68b4e2b0-b1b7-4b0a-8c1a-82ac27c1f12e)
-   [Supresión de archivos de programa de RMS](https://technet.microsoft.com/d1dc8a8b-f8de-487f-87b4-2174d449f0bc)
-   [Alternativas al retiro de RMS](https://technet.microsoft.com/4d32f35e-997d-4d10-ab66-efe217e853f7)
