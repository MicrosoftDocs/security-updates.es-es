---
TOCTitle: Cuestiones de compatibilidad con FIPS para RMS
Title: Cuestiones de compatibilidad con FIPS para RMS
ms:assetid: '720bdace-dcd8-431e-b0fa-01193782fe0b'
ms:contentKeyID: 18127848
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747551(v=WS.10)'
---

Cuestiones de compatibilidad con FIPS para RMS
==============================================

La versión 1.0 de los Servicios de Rights Management (RMS) Service Pack 1 (SP1) está diseñada para funcionar eficazmente en organizaciones que necesitan utilizar la funcionalidad de cifrado conforme a FIPS.

El estándar federal de procesamiento de información 140-1 (FIPS 140-1) y su sucesor FIPS 140-2 son estándares del gobierno de Estados Unidos que proporcionan un punto de referencia para la implementación de software de cifrado. Especifican procedimientos recomendados para implementar algoritmos cifrados, manejar material de clave y búferes de datos, así como para trabajar con el sistema operativo.

RMS puede implementarse como parte de un sistema compatible con FIPS para así ofrecer un modo de proteger los datos confidenciales.

-   Los proveedores de servicios de cifrado conforme a FIPS restringen la funcionalidad a: **TLS\_RSA\_WITH\_3DES\_EDE\_CBC\_SHA**. Esta restricción obliga al proveedor del canal de seguridad a negociar únicamente el protocolo TLS (Transport Layer Security) 1.0 más seguro. Puede ser necesario configurar Internet Explorer para que admita TLS; muchos servidores Web de terceros no son compatibles con TLS. Para obtener más información sobre este tema, vea el artículo 811834 de Knowledge Base en el [sitio Web de Microsoft](http://go.microsoft.com/fwlink/?linkid=43614).

Si va a utilizar la protección de clave privada de software, proteja la clave privada de RMS con uno de los dos proveedores de servicios de cifrado (CSP) predeterminados de Microsoft. Estos CSP han superado el proceso de evaluación FIPS 140-1 o FIPS 140-2 (según convenga) del gobierno de Estados Unidos. Aunque no es imprescindible, es recomendable que los clientes para los que la seguridad es vital utilicen módulos de seguridad de hardware (como los de nCipher o IBM) para proteger las claves privadas del servidor de RMS de alto nivel. Si se utilizan módulos de seguridad de hardware, debe seleccionarse el CSP adecuado para el módulo. Esto puede hacer necesario reiniciar el sistema. Para obtener más información sobre este tema, vea el artículo 830690 de Knowledge Base en el [sitio Web de Microsoft](http://go.microsoft.com/fwlink/?linkid=44138).

Al implementar el sistema RMS, deberá realizar las siguientes selecciones:

-   Siga las instrucciones de la NSA para cifrado conforme a FIPS en Windows.
-   Active la directiva de seguridad local para cifrado conforme a FIPS.
-   Implemente los clientes y servidores de RMS SP1 en este entorno.
-   Habilite el protocolo TLS (Transport Layer Security) en los Servicios de Internet Information Server en el servidor de RMS.
-   Habilite el protocolo TLS (Transport Layer Security) en Internet Explorer para sus clientes.
-   Habilite el protocolo TDS (Tabular Data Stream) de SQL que se utiliza con el proveedor de seguridad TLS/SSL de Windows entre los clientes SQL y el servidor SQL en el servidor de base de datos.
-   Configure SQL para que requiera TSL/SSL.
