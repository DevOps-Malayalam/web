---
layout: post
title:  "Azure For Begineers [EP1] Key Takeaways"
author: Alexy
categories: [ Azure, Cloud, Takeaways, DevOps ]
image: assets/images/azure1.jpg
---
# DevOps Malayalam

## **Azure For Beginners** 
_4 August 21_ <br>
<br>
**Series 1**  <br> <a href="https://www.youtube.com/watch?v=0XMyp4FSnsw"><img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" />
<br> 

## Key Takeaways

### Topics Discussed:
  * History of Azure
  * Azure Cloud Architecture
  * Azure Cloud Account
  * Azure Functions
  * Service Categorisation
  * Getting Started with Azure(Study Materials, Courses)


**[History](https://www.slideshare.net/MattDeacon/a-brief-history-of-azure)** - Earlier we used on-premise data centers for hosting.  For running applications we need infrastructure for its support. <br>
Then the hosted data centers came. Along with it companies started to buy or lease the data centers. Here usually 3 to 5 years of lease is taken. <br>
And the cloud came into action and became popular due to its _pay as you go feature_.It is a helpful platform for start-ups. <br>
2010 - Azure released publicly. <br>

**Virtualization** is the base of Cloud. Then an updated method called Hyper-V was introduced. <br>
By 2014 it became Microsoft Azure, and more projects came into Open source. So the Linix engine was introduced in the azure. <br>
  
A standard was brought for selling Cloud Services.
  * IAAS - Networking is the building blocks or foundation, then comes storage and hypervisor then comes the operation system and finally we implement applications . OS, Run Time Stack, Web Servers are controlled by Customers. This is the shared responsibility. (Eg: Security and backup of OS is managed by the user) Eg: Virtual Machine.
  * PAAS- Web Services Application is the core focus.We need to take care of hosting or Deploying  applications. So all other things including the OS will be taken care by Cloud Providers.
  * SAAS - Eg: Gmail. We don’t want to manage  its underlying  infrastructure.
  

Then the Cloud providers brought Service Level Agreement (SLAs).  For this SLA Azure architecture is set. <br>
World wide data centers are being built. Group of data centers are called **Regions**. Inside each region mini 1 data center and max 3 data centers are available. South India region is the latest in India. In each availability zone we get Availability Sets. Two parts - Update Domain And Fault Domain. We do this by using load balancers. <br>
  
**Region Pair**: Eg: _West Europe_ - _North Europe_. <br>
Each region has a region pair provided new or upcoming regions will not be having region pairs. <br>
When we create an account an azure active directory is created. It's called **Tenant**- Identity management service. <br> 
To access each service we need to take subscriptions. We can add multiple subscriptions into one Azure Tenant. <br>
The **Resource Group** contains all the services we use and we can give individual permission. <br>

## Free Azure Credits For Students :
* Use College Provided Email ID - You get 100 credits for 1 year.
* Use Github Pro([Github Student Developer Pack](https://education.github.com/pack?sort=popularity&tag=Cloud))Account - You get 100 credits for 1 year.

**Management Options** 
  *  [Cloud GUI](https://portal.azure.com/)
  *  Powershell CLI
  *  AZ CLI - Bash based CLI
  *  Cloud Shell - Available at the top in the GUI. Popular tools like Git, docker etc will be  available in it
  *  SDKs - We can connect using the programming languages 

API  is available in each region. API takes the request to the orchestrator and directs it to a specific location or Data center. The fabric controller identifies the availability at the data centers.

[Microsoft Learn](https://docs.microsoft.com/en-in/learn/) A platform by microsoft to learn more about Azure free of cost. <br>
**Getting started with Microsoft Learn** <br>
Create or use existing Microsoft account to login to the Microsoft Learn (Use the Sign-in button on the top right corner before you start the learning, Knowledge check and Labs)
You will be provided with learning points and badges upon completion of each module, at the module the suggestions or path to the next module  will be provided.

```markdown
1. AZ 900 Course - Beginner Level
2. AZ 104 Course - Intermediate Level
3. AZ 204 for Developers
4. AZ 400 and AZ 104 For DevOps Engineers
5. AZ 700 For Networking
```
Basic Idea in IT infrastructure will be helpful for the beginners or looking for a career switch. And they can start with AZ 900 courses. <br>

[Windows Private Cloud](http://www.davidchappell.com/writing/white_papers/The_Microsoft_Private_Cloud_v1.0--Chappell.pdf)
  
###  Free Labs
  * Create a windows Virtual Machine on Azure and access it from your computer/Laptop  using RDP
      1. [Link 1](https://docs.microsoft.com/en-us/learn/modules/create-windows-virtual-machine-in-azure/3-exercise-create-a-vm)
      2. [Link 2](https://docs.microsoft.com/en-us/learn/modules/create-windows-virtual-machine-in-azure/5-exercise-connect-to-a-windows-vm-using-rdp)
  * Create a Linux Virtual Machine on Azure and access it from your computer/Laptop using SSH
      1. [Link 1](https://docs.microsoft.com/en-us/learn/modules/create-linux-virtual-machine-in-azure/4-exercise-create-a-vm)
      2. [Link 2](https://docs.microsoft.com/en-us/learn/modules/create-linux-virtual-machine-in-azure/3-exercise-generate-ssh-key)
      3. [Link 3](https://docs.microsoft.com/en-us/learn/modules/create-linux-virtual-machine-in-azure/6-exercise-connect-to-a-linux-vm-using-ssh)
  
  
### Follow Us On

[LinkedIn](https://www.linkedin.com/company/devopsmalayalam)
[ClubHouse](https://github.com/DevOps-Malayalam/Test/settings/pages)
[Telegram](https://t.me/joinchat/tninMc2bBGdiY2E1)
[Slack](https://join.slack.com/t/devopsmalayalam/shared_invite/zt-tuws4bts-9ZhKh5snDTuv8m7FiECv~g)

### Support or Contact

[Queries❓](https://docs.google.com/forms/d/e/1FAIpQLSdXmOgcM1zqVVONSZkrQ_twl2D9G8UBesN5OJ4xMZj_yXgebg/viewform)
