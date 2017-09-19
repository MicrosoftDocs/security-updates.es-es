---
TOCTitle: Cálculo de crecimiento de base de datos
Title: Cálculo de crecimiento de base de datos
ms:assetid: '87652cc2-b886-4797-8d40-356669768089'
ms:contentKeyID: 18127907
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747585(v=WS.10)'
---

Cálculo de crecimiento de base de datos
=======================================

Al calcular la cantidad de almacenamiento que necesitan las bases de datos de RMS, elabore un plan para una capacidad mínima de 10 megabytes (MB) y, a continuación, agregue un 1 MB por cada 500 usuarios para la base de datos de configuración de RMS. La base de datos de registro puede existir en un servidor de base de datos distinto que la base de datos de configuración.

Si utiliza la característica de registro de RMS, la base de datos de registro necesitará admitir un crecimiento aproximado de 1 MB para cada usuario durante la fase inicial de certificación de usuarios cuando se produzca una gran cantidad de registros. Por ejemplo, en caso de que la implementación admita 1.000 usuarios, la base de datos de registro aumentará hasta 1 gigabyte (GB) a medida que el servidor de certificación de RMS active y certifique estos usuarios. Durante el funcionamiento habitual, la base de datos de registro puede aumentar a una tasa de 200 kilobytes (KB) por usuario y día (en caso de que efectúe una implementación por fases, calcule 1 MB más para cada nuevo usuario que se agregue al sistema.)
