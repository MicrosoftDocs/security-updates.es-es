---
TOCTitle: Create Replica Servers
Title: Create Replica Servers
ms:assetid: '98f0a612-9950-4c1d-ba02-a03ea9db81ef'
ms:contentKeyID: 21741403
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd939885(v=WS.10)'
---

Create Replica Servers
======================

A description of the benefits of creating a replica server is available in "Centralized Management" in [Choose a WSUS Management Style](https://technet.microsoft.com/7a9c8db5-9c94-425a-894d-94e10dad4a51) earlier in this guide.

**To create a replica group for centralized management of multiple WSUS servers**
1.  Install WSUS on a computer at a site where it can be managed by an administrator. Follow the steps in [Run WSUS 3.0 SP2 Server Setup](https://technet.microsoft.com/3bc2933c-8d26-4594-b989-e64b406f3147) in this guide.

2.  Install WSUS on a computer at a remote site, in the same way as in Step 1. When you have launched the Configuration Wizard, go to the **Choose Upstream Server** page, select the **Synchronize from another Windows Server Update Services server** check box, and then enter the name of the WSUS server from step 1.

3.  If you are planning to use SSL for this connection, select the **Use SSL when synchronizing update information** check box.

4.  Select the **This is a replica of the upstream server** check box.

5.  Repeat steps 2, 3, and 4 as necessary to add additional WSUS servers to the replica group.

Enable reporting rollup from replica servers
--------------------------------------------

You can roll up computer and update status from replica servers to their upstream server.

**To enable reporting rollup from replica servers**
1.  In the WSUS administration console on the upstream server, click **Options**, and then **Reporting Rollup**.

2.  Select the **Roll up status from replica downstream servers** check box, and then click **OK**.

 
<p> </p>
> [!NOTE]
> During the client scan, if the server detects the client changed group membership (or name, or IP address, or operating system version), it marks the client as needing a full rollup. The downstream server will roll up these changes to the upstream server during the next rollup after client scan.
