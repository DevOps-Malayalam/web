---
layout: post
title:  "Kubernetes Final Part [CI/CD best practices] Key Takeaways"
categories: [ Kubernetes, Cloud, Takeaways, DevOps ]
image: assets/images/k8s.jpeg
author: sibin
---


_07 August 21_ <br> <a href="https://www.youtube.com/watch?v=pK6vx74szho"><img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" />
<br> 

## Key Takeaways

### Topics Discussed:
  * Micro services
  * Continuous Integration and its tools
    * Kaniko
    * Tekton
  * Github
  * GitOps
  * FluxCD
  * GitOps Advantages
  * Security measures and Vulnerability management
  * Unmanaged vs Managed K8S clusters

**Micro services:** <br>
Independent small applications to build an entire application. <br>
Each micro services are decoupled in nature. <br>
Source code versioning for each apps can achieve using git. <br>
We can have separate Docker files for individual application’s git repo. <br>

**Continuous Integration and its tools:** <br>
We are discussing about two k8s native tools for ci/cd practices **Kaniko** and **tekton**. <br>
* K8S based Continuous Integration will not use “docker build” in K8S due to complexities related to host and docker socket of the host where the CI container run. 
* Also in latest versions of K8S containerD is the default is the runtime instead of docker so it won’t be a good idea to stick on with docker build

**Kaniko:** <br>
Kaniko is a Docker image builder tool. <br>
It will use same docker file to build image like docker do. <br>

**Tekton:** <br>
Tekton is a K8s native CI tool. <br>
It will get advantages of k8s like other k8s native applications. <br>
It can create multiple tasks using CRDs. <br>
For example: <br>
  * Task to clone code from git 
  * Task to build image 
  * Task to push image 
We can customize tasks using parameters and can create ci pipelines using the same. <br>

Pipeline is a set of tasks, which will define tasks step by step. <br>
  * Pipelines can reuse 
  * Pipelines are static resources in k8s
  * Pipeline run can use to parse parameters to the pipeline tasks

Tekton has catalogues to create tasks and it uses yaml syntax. <br>

**How to get reusable steps?** <br>
Go to tekton catalogues - search for kaniko - if it exists can reuse it or else can create our
own. <br>

We can add tasks to push build artifacts to artifactory like **Jfrog**. <br>
  For ex: artifacts of “maven build” <br>
Container **security** scan can add in the steps of CI pipeline. <br>
**Clair** can be used to scan docker images, and we can add this as a step in the tekton tasks. <br>
We can mention docker image and commands to run in tekton tasks as part of tekton topic. <br>
A pipeline formation will include identification of main task to perform and split it to smaller multiple tasks. <br>
Tekton will run each tasks in different pods and it will deploy pods to all possible nodes in the cluster. <br>
And persistent volume will be used to share data in between multiple containers. <br>
Tekton has permission settings to maintain RBAC for users. <br>
Tekton is k8s native so it will avoid manual work complexities like jenkins do like multiple tasks to run in single container. <br>
Tekton is having task as a CRD, and this eaziness will not be there for gitlab or jenkins pods. <br>
It can use as a k8s kind, so its flexible as other k8s native resources. <br>
Tekton will run tasks as pods and it can have multiple containers to run steps. <br>
Tekton can also be used for Continuos Delivery, but it is not advisable due to complexities. But still we can achieve Continuos Delivery using tasks. We can use kubectl client, docker images , and need to add secrets to pass cluster authentication. For this, we need to check for already available catalogue tasks to deploy using kubectl.

**Github & Tekton:** <br>
Tekton can integrate with github for autotriggered builds. <br>
When code change happen github will send webhook to tekton and tekton receive this hook as trigger and will run tasks. <br>
Tekton has an event listener CRD. Using this CRD it will identify the PR and will create resources like pipelines run. <br>
Tekton will parse parameters to run through pipeline run. <br>
Tekton needs a public ingress URL and need to create tasks to execute when it receives a
trigger. <br>

**GitOps:** <br>
In GitOps practice we can deploy apps using helm or kustomize in k8s. <br>
Using helm we can create charts and yaml templates and can parameterize applications for
deployment. <br>
Helm charts will maintain in git repos and can use kubectl or any other tools to deploy. <br>
Here we have another tool called argocd. <br>
Argocd will watch cluster and compare changes with git repo, if any changes identified it will
push the same to the cluster. Argocd is also have a CRD and we will update details like git repo, webhook token etc. <br>
Argo has **automatic prune**, to delete and update resources in cluster. <br>
Cluster state will update in git and desired state will push to cluster using argo. <br>

**FluxCD:** Weaveworks provided operator based tool for gitops. <br>
**Kustomize:** k8s native resource configuration management tool <br>

**Gitops advantages:** <br>
**Autosync** and **manual sync** to cluster state from git repo. <br>
In **Autosync**,  Operator will watch the code changes and will help to autosync Declarative state. <br>
Gitops will help us to have a Developer perspective for operations and can have strategies to segregate deployments to different clusters like a development branch for dev clusters , prod branch for prod clusters… <br>

**Security:** <br>
Vulnerability management for public cloud k8s clusters can be perform by native scanning tools for each cloud provider like gcp, azure etc.. <br>
Ongoing docker scan can initiate from image build step in CI pipeline and **Synk** can use for container image scan. <br>
**Enterprise Synk** can be used to add a remedy for the vulnerability also. <br>
**Falco** is one of the tools for container runtime security. <br>
**Padbot** for security compliance monitoring for the entire platform and runtime. <br>
**Tekton** step can also use to check for vulnerability and if it is vulnerabile we can fail the
pipeline using the tekton task. <br>
**Encrypted rests** can be implemented to improve security of **etcd objects** like **secrets** <br>

**Unmanaged(self managed) vs Managed K8S Clusters:** <br>
Flexibility can achieve as per our decisions in self managed clusters. <br>
Integrations as per our needs in self managed clusters. <br>
Security compliance as we decide in self managed clusters . <br>
Audit events customization is not possible in managed clusters. <br>
Each pod needs an ip in the vpc of the managed cluster but it will be difficult in clusters having a large number of pods. <br>
Encrypted rests can easily achieve in managed cloud but for self managed cluster its complex to implement. <br>

### Follow Us On

[LinkedIn](https://www.linkedin.com/company/devopsmalayalam)
[ClubHouse](https://github.com/DevOps-Malayalam/Test/settings/pages)
[Telegram](https://t.me/joinchat/tninMc2bBGdiY2E1)
[Slack](https://join.slack.com/t/devopsmalayalam/shared_invite/zt-tuws4bts-9ZhKh5snDTuv8m7FiECv~g)


### Support or Contact

[Queries❓](https://docs.google.com/forms/d/e/1FAIpQLSdXmOgcM1zqVVONSZkrQ_twl2D9G8UBesN5OJ4xMZj_yXgebg/viewform)

