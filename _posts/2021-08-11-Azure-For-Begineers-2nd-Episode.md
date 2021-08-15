---
layout: post
title:  "Azure For Beginner Episode-2"
categories: [ Azure, Cloud, Takeaways, DevOps ]
image: assets/images/azure2.jpg
author: alexy
---


Azure [Beginner Series 2] <br>
_11 August 21_ <br> <a href="https://www.youtube.com/watch?v=wYXB-dRahbc"><img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" />
<br> 

## Key Takeaways

### Topics Discussed:
  * Azure Cloud Services
  * Service Categories
  * Azure Cost management
  * Azure RBAC
  * Azure Learning Path

OnPremises services - A web based application needs to be hosted. There we need servers, more precisely we need computers(CPU and Memory). And we need this to be accessed by different people. We make this possible by networking. We need to store data. For this we need storage. Also we need a backend database, in which the data is stored in a structured way. We need minimum these components plus security firewalls, load balancers etc... 

So we are using all these in the Cloud where we don’t want to reserve any of these services.

Azure Cloud - Mainly 10 Categories.
1)    Compute
2)    Networking
3)    Storage
4)    Mobile
5)    Databases
6)    Web
7)    Internet of Things (IoT)
8)    Big data
9)    AI
10)    DevOps <br>
  
We will explore few major foundational services below: 

**Compute Service** : basically a memory and CPU. Infrastructure as a service and Platform as a service.
Virtual Machine ; It's not a single Component. There will be a compute unit which consist of Vcpu and memory, harddisk for OS and data which is obtained from storage services and network interface card with ip address from Network services. <br>
Eg: Virtual machine - IaaS <br>
Kubernetes Service - PaaS <br>
App Service - PaaS <br>
Function - FaaS <br>

For Storing data we use storage service. Azure provides storage services as bundle called Storage Account which consists of 4 types of storages : <br>
**Blob Storage** - (Binary Large Object) which is used for storing high volumes of unstructured data like images, videos, documents etc..
Virtual harddisk are stored under Blob Storage. <br>
**File Share** - Storage that can be minuted as SMP Protocol and NFS Service in the compute.
We purchase a dedicated storage so that the data stored without lose. <br>
File Share - SMP Protocol and NFS Service <br>
We also have a backup service.
**Table** - Table storage for No SQL <br>
**Queue** - Queue storage similar to MSMQ service in onprem <br>
**Archive** is also available to keep the data for longer period of time with minimal cost <br>

**Object Storage or Block Storage** - In on premise storage requirements are catered by leveraging SAN( Storage Area Network), NAS (Network Access Share) etc.. 
In Azure just place the data in storage and it will be managed by providers. <br>
**Blob (Binary Large Object) Storage** - For storing Huge Unstructured data for a long time. <br>
Archive Facility - For keeping data for long years. <br>
Azure - Blob | AWS - S3 <br>
<br>
For networking we are offered Virtual Switches which is a software defined networking switch. <br>
Virtual Networks in Azure called as VNET which consist of many IP address space and can be subdivided into smaller IP addresses called subnets <br>
We can assign IP addresses and subnets. <br>
Virtual Network Gateway service for connecting Onpremise and Cloud. <br>
In two ways we can do this : **VPN** and (Direct Connection) **Express Route** <br>

**Load Balancing** : We have hosterf our application on a single server. And if one server is down obisioly the App service will also be done. We use load balancing to equally divide the services to more servers. Application Gateway - Layer 7 capable. Then a load balancer with a  layer 7 capability. <br>

**Cost Management** - 2 VM with 8gb Ram we need to spend 7/- for an hour. We can’t say Cloud is cost effective to everyone. TCO (Total Cost of Operations) calculator is available in Azure. <br>

**Cross Plane** : Infrastructure provisioning with Kubernates. <br>
  
[TCO calculator](https://azure.microsoft.com/en-in/pricing/tco/calculator)   |    [Pricing Calculator](https://azure.microsoft.com/en-in/pricing/calculator/ )  |   [Certification path ](https://docs.microsoft.com/en-us/learn/certifications)
  
### Follow Us On

[LinkedIn](https://www.linkedin.com/company/devopsmalayalam)
[ClubHouse](https://github.com/DevOps-Malayalam/Test/settings/pages)
[Telegram](https://t.me/joinchat/tninMc2bBGdiY2E1)
[Slack](https://join.slack.com/t/devopsmalayalam/shared_invite/zt-tuws4bts-9ZhKh5snDTuv8m7FiECv~g)


### Support or Contact

[Queries❓](https://docs.google.com/forms/d/e/1FAIpQLSdXmOgcM1zqVVONSZkrQ_twl2D9G8UBesN5OJ4xMZj_yXgebg/viewform)

