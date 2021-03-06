---
TOCTitle: SQL Server and Exchange Server Updates Approval
Title: SQL Server and Exchange Server Updates Approval
ms:assetid: '4d28ab1d-7ef2-46dc-bb9c-e4b9bb9b7e41'
ms:contentKeyID: 18158335
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720535(v=WS.10)'
---

SQL Server and Exchange Server Updates Approval
===============================================

Updating Microsoft SQL Server instances
---------------------------------------

SQL Server installations can become quite complex, with multiple instances or even versions of SQL Server on a single computer. You will need to make sure that when you specify your synchronization options, you account for all the versions of the SQL Server you have on the computer. For more information about configuring synchronization options, see [Setting Up Synchronizations](https://technet.microsoft.com/ea68acc8-c590-4810-b0f0-0acab9f7ec8a).

Updating Microsoft SQL Server and Microsoft Exchange Servers that are part of a cluster
---------------------------------------------------------------------------------------

Both Microsoft SQL Server and Microsoft Exchange Server can be installed in a *clustered environment*. If there is an update available for clustered servers, each server in the cluster must be updated individually. Microsoft recommends that you update passive cluster nodes individually. You will need to stop the cluster service for each server while you update it, and then restart the service.

> [!NOTE]
> You can have both a stand-alone instance and a clustered instance of SQL Server on the same server. If you are updating a server that is running both a stand-alone instance and a clustered instance of SQL server, both SQL Server instances will be updated if you have specified the correct synchronization options. 
