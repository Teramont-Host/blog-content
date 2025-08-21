---
title: SFTP Connection Guide [2025]
date: "2025-08-21"
authorId: "teoremal-dev"
excerpt: "Learn how to connect your files to Teramont.net via SFTP using WinSCP, FileZilla, and CyberDuck quickly and securely."
category: "Tutorials"
tags: [SFTP, Teramont, WinSCP, FileZilla, CyberDuck, Security, Servers, Tutorial]
---

# How to Use SFTP Clients on Teramont.net: WinSCP, FileZilla, and CyberDuck

:::info
This tutorial is designed for Teramont.net users who want to connect their files via SFTP using the Teramont Control Panel (TCP). We will focus exclusively on SFTP, since the panel automatically handles the required configuration. Make sure you have your credentials ready before starting.
:::

## Introduction to SFTP on Teramont.net

SFTP (SSH File Transfer Protocol) is a secure protocol for transferring files between your computer and the Teramont.net server. Unlike FTP, SFTP encrypts the connection, protecting your data. On Teramont.net, SFTP access is easily configured through the Teramont Control Panel (TCP).

To obtain your SFTP credentials:
1. Log into your TCP panel at [https://panel.teramont.net](https://panel.teramont.net).
2. Go to the **Settings** section of the server you want to connect to.
3. Under **SFTP Details**, you will find:
    - **Server Address**: For example, `sftp://mia05.teramont.net:2022` (the subdomain may vary depending on your server).
    - **Username**: A unique identifier, such as `ujmtg9pne3715212`.
    - **Password**: Use the same password you use to access the TCP panel.

Take note! The "Launch SFTP" button in the TCP panel will take you directly to the SFTP setup and quickly launch WinSCP.

![TCP panel screenshot showing SFTP details](https://imgur.com/oRWlSvL.png)

:::warning
Do not share your SFTP credentials with anyone, as they grant full access to your files. Instead, you can create Sub-Users.
:::

> [!TIP]  
> Always update your SFTP clients to the latest version for better security.

Next, we will guide you step by step to connect using three popular clients: WinSCP (for Windows), FileZilla (cross-platform), and CyberDuck (for macOS and Windows).

## Connecting with WinSCP

WinSCP is a free and open-source SFTP client, ideal for Windows users. Download it from [https://winscp.net](https://winscp.net).

### Steps to connect:
1. Install and open WinSCP. The "Login" dialog will appear.
2. In "Protocol," select **SFTP**.
3. In "Host name," enter the server host without the prefix (e.g., `mia05.teramont.net`).
4. In "Port," enter **2022** (or the port indicated in your panel).
5. In "User name," enter your username (e.g., `ujmtg9pne3715212`).
6. In "Password," enter your TCP panel password.
7. Optional: Click "Save" to store the session with a name such as "My Extreme 6GB Server."
8. Click "Login" to connect.

![WinSCP login dialog screenshot](https://imgur.com/eLJgZFy.png)

:::danger
If you receive a connection error, check that the port is correct (2022 instead of the default 22) and that no local firewalls are blocking the connection.
:::

Once connected, you will see remote files on the right panel and local files on the left. Drag and drop to transfer files.

> [!WARNING]  
> Avoid transferring sensitive files without additional encryption if needed.

## Connecting with FileZilla

FileZilla is a free and cross-platform SFTP client. Download it from [https://filezilla-project.org](https://filezilla-project.org).

### Steps to connect (using Quick Connect):
1. Open FileZilla.
2. In the top "Quick Connect" bar:
    - **Host**: Enter `sftp://mia05.teramont.net` (include the `sftp://` prefix).
    - **Username**: Enter your username (e.g., `ujmtg9pne3715212`).
    - **Password**: Enter your TCP panel password.
    - **Port**: Enter **2022**.
3. Click "Quickconnect."

### Alternative: Using Site Manager for saved connections:
1. Go to "File" > "Site Manager."
2. Create a new entry:
    - **Protocol**: Select SFTP.
    - **Host**: `mia05.teramont.net`.
    - **Port**: **2022**.
    - **Logon Type**: Normal.
    - **User**: Your username.
    - **Password**: Your password.
3. Click "Connect."

![FileZilla Quick Connect screenshot](https://imgur.com/pfLnIA0.png)

:::tip
FileZilla saves the last 10 Quick Connect connections for easy reuse.
:::

> [!CAUTION]  
> Do not use SFTP on public networks without a VPN to avoid risks.

## Connecting with CyberDuck

CyberDuck is a free SFTP client, popular on macOS but also available for Windows. Download it from [https://cyberduck.io](https://cyberduck.io).

### Steps to connect:
1. Open CyberDuck and select "File" > "Open Connection" or click the "New Connection" button.
2. In the protocol dropdown, select **SFTP (SSH File Transfer Protocol)**.
3. In "Server," enter the host (e.g., `mia05.teramont.net`).
4. In "Port," enter **2022** (the default is 22, so change it if necessary).
5. In "Username," enter your username (e.g., `ujmtg9pne3715212`).
6. In "Password," enter your TCP panel password.
7. Click "Connect." If it is your first time, accept the host key.

![CyberDuck connection dialog screenshot](https://imgur.com/Y72cTLi.png)

:::info
CyberDuck supports bookmarks for saving frequent connections. Add one after a successful connection.
:::

## I'm already connected! What's next?
Simply drag and drop to transfer files between your computer and the server. You can edit files directly if your client allows it. Fortunately, all of these allow direct editing of files.

## Final Notes

With these steps, you will be able to securely access and manage your files on Teramont.net using SFTP. If you encounter issues, check your credentials in the TCP panel or contact Teramont support. Remember that SFTP is ideal for editing and uploading files, especially large ones (100MB+), allowing fast and secure edits.

:::danger
If you forget your password, reset it in the TCP panel, as it is the same for SFTP.

:::
