---
TOCTitle: Copias de seguridad de sistema para RMS
Title: Copias de seguridad de sistema para RMS
ms:assetid: 'c29894da-ee00-428c-8d48-80d8e5a83678'
ms:contentKeyID: 18127940
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747746(v=WS.10)'
---

Copias de seguridad de sistema para RMS
=======================================

Antes de configurar la infraestructura e instalar RMS, realice una copia de seguridad de los siguientes componentes, según corresponda:

-   Si va a utilizar una base de datos SQL Server existente para alojar las bases de datos de configuración y registro, realice una copia de seguridad de todas las bases de datos existentes y de la configuración del servidor. Si está actualizando una versión anterior de RMS o reinstala RMS, asegúrese de que realiza una copia de seguridad de las bases de datos de configuración y registro anteriores.

-   Haga una copia de seguridad del estado del sistema del servidor donde va a instalar RMS. Esta copia de seguridad almacena las claves y los valores del registro que contienen la información necesaria para restaurar el servidor, si es necesario.

-   Utilice el complemento Certificados para exportar los certificados a un archivo. El complemento Certificados también se utiliza para realizar una copia de seguridad de los datos de una clave privada de RMS en un archivo PKCS \#12 que está cifrado con contraseña. Si está actualizando o reinstalando RMS y eligió el cifrado de software predeterminado para proteger la clave privada de RMS, ésta se ha cifrado y almacenado con la copia de seguridad de la base de datos de configuración.

-   Si ha utilizado un módulo de seguridad de hardware para proteger la clave privada, debe realizar una copia de seguridad de su configuración utilizando los métodos recomendados por el fabricante.

Los archivos de copia de seguridad deben conservarse en una ubicación de almacenamiento segura junto con la contraseña utilizada para cifrar las claves privadas.