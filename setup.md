# Homelab Active Directory Setup Guide

## Overview
This guide will walk you through the steps to set up an Active Directory Domain Controller in a homelab environment. It covers the installation of necessary roles and features, configuration of DNS and DHCP.

## Prerequisites
Before starting, ensure you have the following:

- **Windows Server 2022** installed on your server machine.
- **Administrative Access** to the server.
- **Basic Networking Knowledge**, including understanding of DNS, DHCP, and Active Directory.

## Step 1: Install Active Directory Domain Services (AD DS)

1. **Open Server Manager:**
   - Log in to your Windows Server machine.
   - Click on the Start menu and select "Server Manager."

2. **Add Roles and Features:**
   - In Server Manager, click "Add roles and features."
   - On the "Before you begin" page, click "Next."

3. **Installation Type:**
   - Choose "Role-based or feature-based installation" and click "Next."

4. **Select Destination Server:**
   - Select your server from the server pool and click "Next."

5. **Server Roles:**
   - Check "Active Directory Domain Services."
   - When prompted, click "Add Features," then click "Next."

6. **Feature Selection:**
   - Accept the default features and click "Next."

7. **AD DS Information:**
   - Review the information and click "Next."

8. **Install:**
   - Click "Install" and wait for the installation to complete.

9. **Promote to Domain Controller:**
   - After installation, click "Promote this server to a domain controller" in the notification flag.

## Step 2: Configure Active Directory Domain

1. **Deployment Configuration:**
   - Choose "Add a new forest."
   - Enter your root domain name (e.g., `homelab.local`), then click "Next."

2. **Domain Controller Options:**
   - Select the default options (DNS server, Global Catalog).
   - Set the Directory Services Restore Mode (DSRM) password and click "Next."

3. **DNS Configuration:**
   - Ignore any delegation warnings and click "Next."

4. **Additional Options:**
   - Accept the default NetBIOS name or modify it if necessary, then click "Next."

5. **Paths:**
   - Use default file paths for the database, log files, and SYSVOL. Click "Next."

6. **Review and Install:**
   - Review your selections and click "Install."
   - The server will reboot to complete the process.

## Step 3: DNS and DHCP Configuration

### DNS Setup

1. **Open DNS Manager:**
   - In Server Manager, click "Tools" and select "DNS."

2. **Create a New Zone:**
   - Right-click on "Forward Lookup Zones" and choose "New Zone."
   - Follow the wizard to create a new primary zone for your domain (e.g., `homelab.local`).

3. **Add Host Records:**
   - Right-click the zone you just created, select "New Host (A or AAAA)," and enter the necessary information.

### DHCP Setup (Optional)

1. **Install the DHCP Role:**
   - In Server Manager, go to "Add roles and features" and install the DHCP Server role.

2. **Configure DHCP:**
   - Open DHCP Manager, right-click on "IPv4," and select "New Scope."
   - Follow the wizard to set up a new scope with your desired IP range.

3. **Activate the Scope:**
   - After creating the scope, right-click it and select "Activate."

## Creating Users and Groups
For instructions on creating users and groups, refer to the [Creating Users and Groups](./creating-users-and-groups.md)

## Creating and Managing Group Policies
For instructions on creating and managing group policies, refer to the [Group Policies](./group-policies.md)



