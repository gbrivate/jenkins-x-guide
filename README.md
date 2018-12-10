![s](https://static.imasters.com.br/wp-content/uploads/2018/07/25101608/Jenkins-X-uma-nova-soluc%CC%A7a%CC%83o-de-CICD-para-Kubernetes-%E2%80%93-Parte-02.jpg)

# Jenkins X - Guide

First of all, have a look to [JenkinsX](https://jenkins-x.io) to know more about it.


### Before start, ensure you have installed these tools:

> [Jx](https://jenkins-x.io/getting-started/install/) (Jenkins X CLI)

> [Google Cloud SDK](https://cloud.google.com/sdk/docs/quickstarts) (We will use GKE, but you can use any other AWS, AKS etc.).

> [Kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/) (Kubernetes command-line tool)

> [Git](https://git-scm.com/) (Distributed version control system)


### Check the instalation

By instaling **Jx** you also should get some tools installed such as **kubectl, Helm and Cloud providers**, for more info about what happening after you install **Jx** visit this [link](https://jenkins-x.io/getting-started/install-on-cluster-what-happens/)

In order to double check run the following command:

```
> jx version

jx                 1.3.620
jenkins x platform 0.0.2940
kubectl            v1.10.7
helm client        v2.11.0+g2e55dbe
helm server        v2.11.0+g2e55dbe
git                git version 2.10.1

```
At this point you are ready to go!

###  Setting up a Google Cloud account 

if you do not have one, please [create one for free](https://cloud.google.com/free/)

Set you gcloud account locally from your terminal run



```
gcloud container clusters get-credentials ninjabelt --zone asia-east1-a --project cinq-jx-dojo

COMMON_GMAIL: jxdojocommon@gmail.com/commonpassword
COMMON_GIT: jxdojocommon/commonpassw0rd

```

** This is necessary because you may have other projects, and wen you run Jx create, is very important that you have set up the right gcloud project.

### Creating our first cluster

Using JX to create a cluster into your gcloud project
```
jx init --namespace=jxdojo --provider=gke --username=jxdojocommon@gmail.com --verbose

```


### Table of definitions

Name                | Descrition
------------------  | --------------------
Git                 | The most popular VCS 
Jenkins             | An open source CI / CD automation platform
Jenkins X	          | A subproject of Jenkins, automates CI/CD processes in Kubernetes based systems
Kubernetes          | a.k.a. k8s, open source, distributed management system of containerized applications
Minikube            | A tool to run Kubernetes locally
GitOps              | A set of principles for managing software and infrastructure based on Git
Docker              | A containers management platform
Docker registry     |	A repository to store and distribute Docker containers
Nexus	              | An artifact repository
Helm	              | A package manager for Kubernetes
Helm Chart          | A collection of configuration files that describe a related set of Kubernetes resources. E.g. chart.
Chartmuseum	        | An open-source Helm Chart Repository
Monocular	          | An open-source web-based UI for Helm Chart management
Quickstart          | Pre-made Jenkins X applications templates a developer can start a project from, instead of starting from scratch



