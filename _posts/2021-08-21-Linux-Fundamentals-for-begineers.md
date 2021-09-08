---
layout: post
title:  "Linux Fundamentals Key Takeaways"
author: alexy
categories: [Cloud, Takeaways, DevOps, linux ]
image: assets/images/linux.jpeg
---

_18 August 21_ <br>
<br>
<br> <a href="https://www.youtube.com/watch?v=hEN8864lJtI"><img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" />
<br> 

## Key Takeaways

### Topics Discussed:
  * Introduction 
  * Linux Philosophy and Concept
  * Man help and info 
  * Login and sudo 
  * Command-line Operations 
  * Text Editor 
  * User Environment 
  * Text Operations 
  * File Operations


We use Operating Systems which is mainly used to  interact with different components or make use of the networking .
Some say Linux is a complete OS. Others say it's only a kernel <br>

**Kernel** is the 1st program loaded to the memory. It stays in the memory till we reboot or shutdown and there will only be one kernel at a time. Kernel is used to manage all the resources. <br>

**Shell** is the program that interacts with users. There can be more than one shell in an OS. Redhat Linux, Ubuntu Linux, Centos Linux etc <br>

**BASH Shell** is the default shell in Centos. It is an interface between user and kernel. Bash is one of the advanced versions among different shells. <br>

*Now we have GUI. But if you are learning linux don’t go for GUI. Use the shell to interact with Linux.*

* Linux is a case sensitive OS.
* Everything in Linux is a file. We make changes in File. 
* It is a modular OS, which means you can load modules or unload modules.

**Three types of users :** 
* Normal User  
* Super or Root User 
* System User

Everything in linux is mapped with numbers.
ID 1- 999 is reserved for system users. User with ID ‘0’ is Super User. Normal users id starts above 1000. <br>
There is by default only one root account, in case we need a user to permanently act like a root user, we can do that by assigning uid 0 to that particular user. <br>
Inbuilt text editors like vim/vi are used as default text editors. <br>

**Vim tutor** - For understanding about vim.

**7 Types of Files** 
* Directory - The ls command is used to list the names of files and directories.
* Normal Files - ‘-’
* Link Files - Hard link and Soft link
* Character File
* Block File
* S File - Sococket File
* P File -Pipe Files

**How to get/take help ?** (As of now we are getting help for ls)
 1. Help cmd : ls --help
 2. Man cmd :  man ls (manual pages) man man will tell you how to use man cmd
 3. Info Pages

Who is the **owner** of File? <br>
Suppose we create a file. It is accessible to 3 people 
* Owner/user 
* Group
* Others

**File Permissions**
The command to change permission is  `chmod`  <br>
Basically each file have 3 permissions
* Read - You can read the file
* Write - You can write/modify the file
* Execute - You can run the file as a script

Directory is also a file. A execute permission to directory means we can enter into directory. If no execute permission we can’t `cd`  into it. <br>
We can change permissions using +,-.= these symbols. You can add permission, remove permission, assign permission. <br>

* Add Permission can be done  by  ‘+’ symbol
* Remove Permission can be done  by  ‘-’ symbol
* Assign Permission can be done  by ‘=’ symbol
Eg: To give write permission to owner -  `u+w<space><filename>` <br>

We can use `touch` cmd to create a file. But it’s real purpose is to update the timestamp.  <br>
`umask` cmd - Setting of default permission <br>
`ls - l`  shows all the permissions. By default there is 1 owner for a file. <br>

**Stripe Down versions of Linux.**
OpenWRT in the Router <br>
D2H Box contains  <br>

### Follow Us On

[LinkedIn](https://www.linkedin.com/company/devopsmalayalam)
[ClubHouse](https://github.com/DevOps-Malayalam/Test/settings/pages)
[Telegram](https://t.me/joinchat/tninMc2bBGdiY2E1)
[Slack](https://join.slack.com/t/devopsmalayalam/shared_invite/zt-tuws4bts-9ZhKh5snDTuv8m7FiECv~g)

### Support or Contact

[Queries❓](https://docs.google.com/forms/d/e/1FAIpQLSdXmOgcM1zqVVONSZkrQ_twl2D9G8UBesN5OJ4xMZj_yXgebg/viewform)
