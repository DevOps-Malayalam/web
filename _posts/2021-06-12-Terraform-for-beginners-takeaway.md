---
layout: post
title:  "Terraform For Begineers - Takeaway"
author: Alexy
categories: [ Terrafrom, Devops, Takeaway ]
image: assets/images/1.jpg
external_url: https://www.linkedin.com/events/kubernetes-finalpart6829708553163567104/
---

_28 July 21_ 
<br> <a href="https://www.youtube.com/watch?v=5Sghd7vY6XA"><img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" />
<br> 

## Key Takeaways


**Infrastructure as a Code** -  For provisioning, configuring and managing services. <br>
Open Source, written in Go and developed by Hashicorp. We can deploy resources in the cloud using code. We can use terraform  for this process. <br>
For provisioning we use terraform, for configuring we use Ansible. <br>
**Terraform three main parts** - A core engine, tf file, provider. <br>
The 1st operation is refresh which is done by the core engine. It checks according to the request. Then it will Plan and after that it will Apply. These are Day 1 activities <br>
Configuration or creation will be day 2 activity. We refresh to check whether it is present and also check the state. And it’s decided and at last it will plan and apply. <br>

**State file and Provider** <br>
Provider helps us for provisioning, core can’t perform these types of wider activities. Providers of AWS can use the target services using APIs. <br>
Providers define a set of resource types(EC2 instance) and data source(details about resource). <br>
Additional file we can see in our tf file is the state file. It captures the real world entity. And when we destroy and apply again, this state file helps in provisioning <br>
A state lock file is also associated, it locks when we apply the build. So that if any change is made in between it will not be affected.<br>

**Terraform config file**
It's a declaration. It's designed by hashicorp and we save it as a .tf file.  There will be a file like main.tf file. The core can understand these types of files. 
Module is also can be written in the main.tf file. 

**Terraform implementation**
We use terraform cmds in our CLI. <br>
After writing a config file the first step we do is```terraform init``` command. <br>
The we use```terraform validate``` <br>
Next we use the ```terraform plan``` which says what we have requested. It's like a summary or details we are implementing
At last we use ```terraform Apply``` then our build starts <br>
```terraform destroy``` we use to destroy what we have built. <br>

**State Management**
There will be a state file in the code. It contains consolidated details. <br>
Best practice is to use the state file locally. <br>
```terraform refresh``` checks the real world state and gives the update. <br>
State push to push from local to remote. <br>

**Terraform Cloud**
It does state management, so no need to bother about real world platforms. <br>
It contains the state file  details as logs. <br>

**Credential passing** 
Underlying instances we manage using IAM roles. <br> 
KMS in AWS, Vault by terraform can be used. <br>



### Follow Us On

[LinkedIn](https://www.linkedin.com/company/devopsmalayalam)
[ClubHouse](https://github.com/DevOps-Malayalam/Test/settings/pages)
[Telegram](https://t.me/joinchat/tninMc2bBGdiY2E1)
[Slack](https://join.slack.com/t/devopsmalayalam/shared_invite/zt-tuws4bts-9ZhKh5snDTuv8m7FiECv~g)

### Support or Contact

[Queries❓](https://docs.google.com/forms/d/e/1FAIpQLSdXmOgcM1zqVVONSZkrQ_twl2D9G8UBesN5OJ4xMZj_yXgebg/viewform)