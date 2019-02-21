# SNP Cloud Workshop
<div class="MCWHeader1">
Continuous delivery in Azure DevOps
</div>

<div class="MCWHeader2">
Before the hands-on lab setup guide
</div>

<div class="MCWHeader3">
January 2019
</div>

© 2019 SNP Technologies Inc. All rights reserved.

**Contents**

<!-- TOC -->

- [Continuous delivery in Azure DevOps before the hands-on lab setup guide for on-premise IIS and SQL](#continuous-delivery-in-azure-devops-before-the-hands-on-lab-setup-guide-for-on-premise-iis-and-sql)
  - [Requirements](#requirements)
  - [Before the hands-on lab](#before-the-hands-on-lab)
    - [Prerequisites](#prerequisites)
    - [Task 1: Configure a development environment](#task-1-configure-a-development-environment)
    - [Task 2: Disable IE enhanced security](#task-2-disable-ie-enhanced-security)
    - [Task 3: Validate connectivity to SQL database](#task-3-validate-connectivity-to-sql-database)

<!-- /TOC -->

# Continuous delivery in Azure DevOps before the hands-on lab setup guide for on-premise IIS and SQL

## Requirements

1.  Microsoft Azure DevOps organisation and accounts.

2.  Client - For developer - Local machine or a server configured with: 

    -   Visual Studio Community 2017
    
    -   SQL Server Management Studio (Optional)

2.  Servers - For hosting/deployment - Local machine or a server configured with:

    -   Powershell with Administrator privileges
    
    -   IIS
    
    -   SQL Server (Same/Different machine)

## Before the hands-on lab

Duration: 30 minutes

In this lab, you will create a developer environment and download the required files for this course if you do not already have one that meets the requirements.

### Prerequisites

-   Microsoft Azure Devops account <https://azure.microsoft.com/en-in/services/devops/>

-   Client computer with Windows 7 or later with Visual Studio 2017

### Task 1: Configure a development environment

If you do not have a machine setup with Visual Studio 2017 Community, complete this task.

1.  At the Azure web portal, create a virtual machine in Azure using the Visual Studio Community 2017 on Windows Server 2016 image.

    ![This is a screenshot of a results window of a search on visual studio community 2017. The results table has the following columns: Name, Publisher, and Category. The second result is highlighted and has the following values: Visual Studio Community 2017 on Windows Server 2016 (x64), Microsoft, and Compute.](images/Setup/image3.png "Virtual machine creation screenshot")

    > It is **highly** recommended to use a DS2_v2 or D2s_v3 instance size for this VM.

    > You will also need to make sure to enable RDP (port 3389) inbound access to the VM.

### Task 2: Disable IE enhanced security

>**Note:** Sometimes this image has IE ESC disabled, and sometimes it does not.

1.  On the new VM, you just created click the Server Manager icon.

    ![Server Manager icon is highlighted on the taskbar.](images/Setup/image4.png "Server Manager icon")

    Click Local Server.

    ![Local Server is selected and highlighted in the Server Manager menu.](images/Setup/image5.png "Server Manager menu")

2.  On the right side of the pane, click **On** by IE Enhanced Security Configuration.

    ![Next to IE Enhanced Security Configuration, On is highlighted.](images/Setup/image6.png "IE Enhanced Security Configuration On")

3.  Change to **Off** for Administrators, and click **OK**.

    ![In the Internet Explorer Enhanced Security Configuration dialog box, under Administrators, Off is selected and highlighted. At the bottom, the OK button is highlighted.](images/Setup/image7.png "Internet Explorer Enhanced Security Configuration dialog box")

### Task 3: Validate connectivity to SQL database

1.  From within the virtual machine, Launch Visual Studio 2017 and validate that you can login with your Microsoft Account when prompted.

  - Launch Visual Studio, open SQL Server Object Explorer from the View menu, and ensure you can connect to your SQL server using SQL authentication.
  
    ![In SQL Server Object Explorer, the submenu for the SQL Server displays with the following options: Refresh, Connect to SQL Server, Manage and Filter Subscriptions, and Open Getting Started Page.](images/Setup/image8.png "SQL Server Object Explorer")

2. Launch SQL Server Management Studio, ensure you can connect to your SQL server using SQL authentication.

    ![In SSMS, Connect to SQL Server.](images/Setup/image8a.png "SSMS")

**Download the exercise files**

1.  Download the exercise files for the training (from within the virtual machine).

    -   Create a new folder on your computer named **C:\\Hackathon**.

    -   Download the support files (.zip format), https://improjectfilescw.blob.core.windows.net/countrywidedemoproject/CWdemo.zip to the new folder.

    -   Extract the contents to the **C:\\Hackathon** folder.


You should follow all steps provided *before* attending the hands-on lab.
