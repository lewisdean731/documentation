---
title: How to securely manage permissions for a specific vApp | UKCloud Ltd
description: Shows how to extend permissions to users for a specific vApp, ensuring that those users cannot also access other vApps or settings within vCloud Director
services: vmware
author: Steve Hall
toc_rootlink: How To
toc_sub1: 
toc_sub2:
toc_sub3:
toc_sub4:
toc_title: Securely manage permissions for a specific vApp
toc_fullpath: How To/vmw-how-manage-vapp-permissions.md
toc_mdlink: vmw-how-manage-vapp-permissions.md
---

# How to securely manage permissions for a specific vApp

## Overview

This guide shows you how to extend permissions to users for specific vApps, while ensuring that those users cannot access other vApps or settings within vCloud Director.

## Prerequisites

You must be able to log in to the UKCloud Portal as an administrator to perform the steps in this guide. If you do not have the appropriate permissions, contact your administrator.

For each user to whom you want to grant permissions on the vApp, you need the vCloud Director user ID. Users can obtain their user ID as follows:

1. Log into the Portal as the appropriate user.

2. Click the drop down list in the top right of the Portal pane and click **API**.

    ![API](images/vmw-portal-mnu-api.png)

3. For the vOrg to which the vApp belongs, make a note of the user ID.

    The user ID is the first part of the **Username** (that is, the part before the @ sign).

    ![Username](images/vmw-portal-api-details.png)

## Managing permissions for a vApp

### Using the HTML5 tenant portal in vCloud Director 9.1

To manage permissions for a specific vApp:

1. Log in to the UKCloud Portal as an administrator.

2. Select the account to which the vApp belongs.

3. In the left-hand menu, click **Contacts** and then **All Contacts**.

    ![contacts](images/ptl-menu-all-contacts.png)

4. Edit the users to whom you want to grant permissions and ensure that only the **vApp User** option is selected for the vOrg to which the vApp belongs.

    ![vApp user](images/manage-image-4.png)

    You can also create new users if required.

5. In the left‑hand menu, click **VMware Cloud** and then the vOrg to which the vApp belongs.

    ![Compute](images/vmw-portal-mnu-compute-services.png)

6. On the **vCloud Director** tab, enter your password and click **Confirm** to access the vCloud Director console.

   ![vCloud Director](images/vmw-portal-vcd-login.png)

7. Click the VDC where your vApp is located.

8. Click the **Details** option within the vApp.

    ![Details option](images/vmw-vcd-tp-vapp-details.png)

9. In the *Sharing* section, select **Share with specific users or groups**.

    ![vApp permissions](images/vmw-vcd-tp-vapp-share.png)

10. For each user to whom you want to grant permissions:

    - Highlight the user or users from the list and go to the right panel to select Access Level.
    - Select the appropriate permission level from the **Access level** list: **Read Only** or **Full Control**.

    ![vApp Access Level](images/vmw-vcd-tp-vapp-share-level.png)

11. When you're done setting permissions for all users, click **Save**.

### Using the Flex-based UI in vCloud Director 8.20

To manage permissions for a specific vApp:

1. Log in to the UKCloud Portal as an administrator.

2. Select the account to which the vApp belongs.

3. In the left-hand menu, click **Contacts** and then **All Contacts**.

    ![contacts](images/ptl-menu-all-contacts.png)

4. Edit the users to whom you want to grant permissions and ensure that only the **vApp User** option is selected for the vOrg to which the vApp belongs.

    ![vApp user](images/manage-image-4.png)

    You can also create new users if required.

5. In the left‑hand menu, click **VMware Cloud** and then the vOrg to which the vApp belongs.

    ![Compute](images/vmw-portal-mnu-compute-services.png)

6. On the **vCloud Director** tab, enter your password and click **Confirm** to access the vCloud Director console.

   ![vCloud Director](images/vmw-portal-vcd-login.png)

7. Right-click the vApp and select **Properties**.

   ![Properties](images/manage-image-7.png)

8. Click the **Sharing** tab and then click **Add Members**.

   ![Add members](images/manage-image-8.png)

9. Select **Specific users and groups**.

10. For each user to whom you want to grant permissions:

    - Enter the user ID and click the **Refresh** icon.

        For information about how to obtain the user ID, see the
        Prerequisites section earlier in this guide.

        ![Specific users](images/manage-image-9.png)

    - In the top table, select the user ID and click **Add**.

        ![Add](images/manage-image-10.png)

    - In the bottom table, select the user ID and then select the appropriate permission level from the **Access level** list: **Read Only**, **Read / Write**, **Full Control**.

        ![Access level](images/manage-image-11.png)

        Read / Write access gives users the ability to power the VM on and off and launch VMRC.

11. When you have finished setting permissions for all users, click **OK**.

## Feedback

If you have any comments on this document or any other aspect of your UKCloud experience, send them to <products@ukcloud.com>.