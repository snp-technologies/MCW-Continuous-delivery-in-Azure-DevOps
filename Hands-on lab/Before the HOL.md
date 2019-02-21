![](https://github.com/Microsoft/MCW-Template-Cloud-Workshop/raw/master/Media/ms-cloud-workshop.png "SNP Cloud Workshops")

<div class="MCWHeader1">
Continuous delivery in Azure DevOps
</div>

<div class="MCWHeader2">
Before the hands-on lab setup guide
</div>

<div class="MCWHeader3">
January 2019
</div>


Information in this document, including URL and other Internet Web site references, is subject to change without notice. Unless otherwise noted, the example companies, organizations, products, domain names, e-mail addresses, logos, people, places, and events depicted herein are fictitious, and no association with any real company, organization, product, domain name, e-mail address, logo, person, place or event is intended or should be inferred. Complying with all applicable copyright laws is the responsibility of the user. Without limiting the rights under copyright, no part of this document may be reproduced, stored in or introduced into a retrieval system, or transmitted in any form or by any means (electronic, mechanical, photocopying, recording, or otherwise), or for any purpose, without the express written permission of Microsoft Corporation.

Microsoft may have patents, patent applications, trademarks, copyrights, or other intellectual property rights covering subject matter in this document. Except as expressly provided in any written license agreement from Microsoft, the furnishing of this document does not give you any license to these patents, trademarks, copyrights, or other intellectual property.

The names of manufacturers, products, or URLs are provided for informational purposes only and Microsoft makes no representations and warranties, either expressed, implied, or statutory, regarding these manufacturers or the use of the products with any Microsoft technologies. The inclusion of a manufacturer or product does not imply endorsement of Microsoft of the manufacturer or product. Links may be provided to third party sites. Such sites are not under the control of Microsoft and Microsoft is not responsible for the contents of any linked site or any link contained in a linked site, or any changes or updates to such sites. Microsoft is not responsible for webcasting or any other form of transmission received from any linked site. Microsoft is providing these links to you only as a convenience, and the inclusion of any link does not imply endorsement of Microsoft of the site or the products contained therein.

© 2019 Microsoft Corporation. All rights reserved.

Microsoft and the trademarks listed at <https://www.microsoft.com/en-us/legal/intellectualproperty/Trademarks/Usage/General.aspx> are trademarks of the Microsoft group of companies. All other trademarks are property of their respective owners.

**Contents**

<!-- TOC -->

- [Continuous delivery in Azure DevOps before the hands-on lab setup guide for on-premise IIS and SQL](#continuous-delivery-in-azure-devops-before-the-hands-on-lab-setup-guide-for-on-premise-iis-and-sql)
  - [Requirements](#requirements)
  - [Before the hands-on lab](#before-the-hands-on-lab)
    - [Prerequisites](#prerequisites)
    - [Task 1: Configure a development environment](#task-1-configure-a-development-environment)
    - [Task 2: Disable IE enhanced security](#task-2-disable-ie-enhanced-security)
    - [Task 3: Validate connectivity to Azure](#task-3-validate-connectivity-to-azure)
    - [Task 4: Download and install Git](#task-4-download-and-install-git)

<!-- /TOC -->

# Continuous delivery in Azure DevOps before the hands-on lab setup guide for on-premise IIS and SQL

## Requirements

1.  Microsoft Azure DevOps organisation and accounts.

2.  Developer - Local machine or a virtual machine configured with: 

    -   Visual Studio Community 2017
    
    -   SQL Server Management Studio (Optional)

2.  Servers - Local machine or a virtual machine configured with:

    -   Powershell with Administrator privileges
    
    -   IIS
    
    -   SQL Server 

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

2.  Validate connectivity to your SQL server with either of following options. 

  - Launch Visual Studio, open SQL Server Object Explorer from the View menu, and ensure you can connect to your SQL server using SQL authentication.
  
  - Launch SQL Server Management Studio, ensure you can connect to your SQL server using SQL authentication.

    ![In Visual Studio Server Explorer, the submenu for the Azure subscription displays with the following options: Refresh, Connect to Microsoft Azure Subscription, Manage and Filter Subscriptions, and Open Getting Started Page.](images/Setup/image8.png "Visual Studio Server Explorer")

**Download the exercise files**

1.  Download the exercise files for the training (from within the virtual machine).

    -   Create a new folder on your computer named **C:\\Hackathon**.

    -   Download the support files (.zip format), https://improjectfilescw.blob.core.windows.net/countrywidedemoproject/CWdemo.zip to the new folder.

    -   Extract the contents to the **C:\\Hackathon** folder.


You should follow all steps provided *before* attending the hands-on lab.
