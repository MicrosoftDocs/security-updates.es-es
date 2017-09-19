---
TOCTitle: Planeamiento de la implementación entre bosques
Title: Planeamiento de la implementación entre bosques
ms:assetid: '2dfb40b7-95b1-4362-b32e-72867544b705'
ms:contentKeyID: 18127774
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720233(v=WS.10)'
---

Planeamiento de la implementación entre bosques
===============================================

Si está implementando RMS en un entorno con varios bosques, debe determinar el soporte que necesitarán los usuarios o los grupos que se encuentran fuera del bosque en el que se implementa RMS. El problema es que los objetos de grupo o usuario de otros bosques no suelen tener objetos representativos en el bosque en el que reside RMS. Si piensa utilizar RMS para restringir los permisos de los usuarios o grupos de otros bosques, debe configurar el bosque adecuadamente para permitir que se produzca la expansión de grupos entre bosques.

Puede implementar la expansión de grupos entre bosques para RMS de dos formas:

-   Implementar RMS en el bosque donde los grupos están definidos y donde se utilizará para ampliar la pertenencia de esos grupos.
-   Sincronizar las definiciones de grupo entre bosques para permitir que la instalación de RMS local determine la pertenencia a grupos completa de cualquier usuario. Si el usuario que solicita una licencia de uso tiene una cuenta de Windows en un bosque distinto, deberá haber un objeto de contacto en el bosque local para representar la pertenencia a ese grupo del usuario. Puede utilizar metadirectorios, como Microsoft® Identity Integration Server (MIIS) 2003 o Identity Integration Feature Pack (IIFP), para implementar la sincronización de fidelidad total de los objetos de grupo entre bosques.

Si tiene previsto utilizar RMS sólo para un bosque, puede optimizar el proceso de emisión de licencias de uso modificando la directiva de clúster **MaxCrossForestCalls** de la base de datos de configuración de RMS. Esta directiva especifica el número máximo de veces que los miembros de un grupo pueden cruzar los límites de los bosques. El valor predeterminado es 10. Para cambiar ese valor por 0, utilice el siguiente comando SQL:

`update DRMS_ClusterPolicies set PolicyData=0 donde PolicyName='MaxCrossForestCalls'`
