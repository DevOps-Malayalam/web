---
layout: post
title:  "Virtual Private Cloud"
author: alexy
categories: [ VPC, Devops, DevOps, Takeaway ]
image: assets/images/3.jpg
---

_21 July 21_ 

## Key Takeaways


### Topics Discussed:
 * VPC/VNet 
 * Subnets- Public and Private Subnet 
 * Routing, Route Tables, Internet Gateway and Nat Gateway 
 * Access Control - Security Group, NACL 
 * VPC Peering     
 * OnPremise Connectivity


**VPC - AWS  | VNet - Azure**
**VPC** - Creating our networks in a private environment. We assign IP range so it's basically our private network.
3 Tier Architecture -  Web Service Layer, Application Layer, Database Layer
Outside world can access only the web layer and through the web layer only we can access the Application Layer. We can do this using VPC.
Default VPC IP is exposed so a better approach is to create a new VPC.
We interact with the outside world with Internet Gateway and we use different services by creating the subnets. We can include these Layers in 3 subnets.
We can create more than 1 VPC.

**Routing** - Communicating within a particular network . We have a set of rules. And the route table helps to set different routing rules. Eg: Internet Gateway and Nat Gateway. <br>
      NAT - Outbound Traffic. Used usually with Database Layer. <br>
      Internet - Both Inbound and Outbound.

**Security Group** - We can allow different port rules. No denying port rules are available.
We need to allow different protocols and set port range. 

**NACL** - Each subnet can be associated  only with  single NACL at a time. But single NACL can be set to different Subnets.
Rule Number - Asterisk(*) This rule ensures that if a packet doesn't match any of the other numbered rules, it's denied. You can't modify or remove this rule.
Adding names for  security groups and descriptions for  rules  is a best practice.

**VPC Peering** - Communicating between another VPCs( peering - data sharing)
When merging two companies, we may have to implement VPC Peering.
Only the owner of VPC can do VPC peering.  Send the VPC request to another VPC and the second VPC accepts it. 
Consider VPCs A,B,C. If A is peered with B and A is peered with C, it doesn’t mean that B and C are connected.  Transit Gateways are a good alternative to connect multiple VPCs
After perring a route table update is needed. 

Direct Connect - Establish private connection from OnPremise to AWS.  



### Follow Us On

[LinkedIn](https://www.linkedin.com/company/devopsmalayalam)
[ClubHouse](https://github.com/DevOps-Malayalam/Test/settings/pages)
[Telegram](https://t.me/joinchat/tninMc2bBGdiY2E1)
[Slack](https://join.slack.com/t/devopsmalayalam/shared_invite/zt-tuws4bts-9ZhKh5snDTuv8m7FiECv~g)

### Support or Contact

[Queries❓](https://docs.google.com/forms/d/e/1FAIpQLSdXmOgcM1zqVVONSZkrQ_twl2D9G8UBesN5OJ4xMZj_yXgebg/viewform)
