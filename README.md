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


### At this point you are ready to go!

