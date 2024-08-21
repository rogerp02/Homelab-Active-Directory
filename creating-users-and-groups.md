# Creating Users and Groups

This guide provides instructions for setting up Organizational Units (OUs), Groups, and Users in your Active Directory environment.


## Prerequisites

Before you begin, ensure you have the following:

- A Windows Server 2022 machine set up and running.
- Administrative privileges on the server.

## Creating Organizational Units (OUs)

1. **Open Active Directory Users and Computers:**
   - Press `Windows + R`, type `dsa.msc`, and press Enter.

2. **Create OUs:**
   - Right-click your domain (e.g., `homelab.local`), select **New** > **Organizational Unit**.
   - Name the OU (e.g., `Users`).
   - Click **OK**.

   **Repeat this process for any other OUs you need.**

## Creating Groups and Users

### Creating Groups

1. **Open Active Directory Users and Computers:**
   - Press `Windows + R`, type `dsa.msc`, and press Enter.

2. **Create Groups:**
   - Right-click the OU where you want to create the group (e.g., `Users`), select **New** > **Group**.
   - Enter the group name (e.g., `IT`, `HR`, `Sales`).
   - Select the group scope (e.g., **Global**).
   - Click **OK**.

   **Repeat this process for each group you need.**

### Creating Users

To create users manually:

1. **Open Active Directory Users and Computers:**
   - Press `Windows + R`, type `dsa.msc`, and press Enter.

2. **Create Users:**
   - Right-click the OU where you want to create the user (e.g., `Users`), select **New** > **User**.
   - Enter the user details:
     - **First Name**: John
     - **Last Name**: Doe
     - **User logon name**: jdoe
   - Click **Next**.
   - Set the password for the user and configure password options as needed.
   - Click **Next**, then **Finish**.

   **Repeat this process for each user you need to create.**

   **Add Users to Groups:**
   - Right-click the user account, select **Add to a group**.
   - Enter the group name (e.g., `IT`, `HR`, `Sales`).
   - Click **OK**.

   **Repeat this process to add users to the appropriate groups.**

