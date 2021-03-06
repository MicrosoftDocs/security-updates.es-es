---
TOCTitle: Personalize the WSUS Display
Title: Personalize the WSUS Display
ms:assetid: 'c16668f3-8671-4372-b669-2fca38f491e6'
ms:contentKeyID: 21741436
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd939895(v=WS.10)'
---

Personalize the WSUS Display
============================

You can configure different aspects of the way WSUS server information is displayed in the WSUS Administration console. You can display information from downstream replica servers when you view computer and update status information. You can have validation errors displayed as pop-up windows. And you can display different types of information in the computer overview's **To Do** section.

**To display rollup data from downstream replica servers**
1.  From the WSUS Administration console, click **Options**, and then click **Personalization**.

2.  On the **General** tab, select the **Include computers and status from replica downstream servers** check box.

3.  Click **OK**.

 
<p> </p>
> [!IMPORTANT]
> Computer and update status will roll up from downstream replica servers only. It is not possible to get rolled-up status from a downstream autonomous server.
 

**To display validation errors as pop-up windows**
1.  From the WSUS Administration console, click **Options**, and then click **Personalization**.

2.  On the **General** tab, select the **Show validation errors as popups** check box.

3.  Click **OK**.

 
<p> </p>
> [!NOTE]
> If you choose this option, errors will appear as pop-up windows and not as links in the UI.
 

**To display different information in the To Do section**
1.  From the WSUS Administration console, click **Options**, and then click **Personalization**.

2.  On the **To Do List** tab, select one or more of the following items:

    -   **Computers have not reported status for more than 30 days**
    -   **WSUS updates are waiting to be approved for install**
    -   **Critical updates are waiting to be approved for install**
    -   **Computers have requested nonexistent computer groups**
    -   **The server database is almost full**
    -   **SSL is not enabled**
    -   **New products and new classifications have been added in the past 30 days**
    -   **Update file languages are enabled on this server, but are no longer supported by the upstream server**

3.  Click **OK**.
