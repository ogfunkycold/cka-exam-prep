[![License: CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/80x15.png)](https://creativecommons.org/licenses/by-sa/4.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

# ☸️ My Preparation for the Certified Kubernetes Administrator (CKA) Exam

This summary provides the curriculum outline of the Knowledge, Skills and Abilities that a Certified Kubernetes Administrator (CKA) can be expected to demonstrate.

## CKA EXAM Curriculum

### 25% - Cluster Architecture, Installation & Configuration

- Manage role based access control (RBAC)
- Use Kubeadm to install a basic cluster
- Manage a highly-available Kubernetes cluster
- Provision underlying infrastructure to deploy a Kubernetes cluster
- Perform a version upgrade on a Kubernetes cluster using Kubeadm
- Implement etcd backup and restore

### 15% - Workloads & Scheduling

- Understand deployments and how to perform rolling update and rollbacks
- Use ConfigMaps and Secrets to configure applications
- Know how to scale applications
- Understand the primitives used to create robust, self-healing, application deployments
- Understand how resource limits can affect Pod scheduling
- Awareness of manifest management and common templating tools

### 20% - Services & Networking

- Understand host networking configuration on the cluster nodes
- Understand connectivity between Pods
- Understand ClusterIP, NodePort, LoadBalancer service types and endpoints
- Know how to use Ingress controllers and Ingress resources
- Know how to configure and use CoreDNS
- Choose an appropriate container network interface plugin

### 10% - Storage

- Understand storage classes, persistent volumes
- Understand volume mode, access modes and reclaim policies for volumes
- Understand persistent volume claims primitive
- Know how to configure applications with persistent storage

### 30% - Troubleshooting

- Evaluate cluster and node logging
- Understand how to monitor applications
- Manage container stdout & stderr logs
- Troubleshoot application failure
- Troubleshoot cluster component failure
- Troubleshoot networking


```
Cloud native computing uses an open source software stack to deploy applications as microservices, 
packaging each part into its own container, and dynamically orchestrating those containers 
to optimize resource utilization. The Cloud Native Computing Foundation (CNCF) hosts critical 
components of those software stacks including Kubernetes, Fluentd, Linkerd, Prometheus, 
OpenTracing and gRPC; brings together the industry’s top developers, end users, and vendors; 
and serves as a neutral home for collaboration. CNCF is part of The Linux Foundation, 
a nonprofit organization. For more information about CNCF, please visit: https://cncf.io/.

CNCF encourages training companies to align their offerings to cover the contents of the
curriculum.  Training [partners](https://www.cncf.io/certification/training/) can purchase 
coupons for the CKA exam at a wholesale price to offer at the end of their training.
```
## Exam resources

- [Candidate Handbook](https://training.linuxfoundation.org/go/cka-ckad-candidate-handbook)
- [Curriculum Overview](https://github.com/cncf/curriculum)   (The latest curriculum can always be found here...)
- [Exam Tips](http://training.linuxfoundation.org/go//Important-Tips-CKA-CKAD)
- [Frequently Asked Questions](http://training.linuxfoundation.org/go/cka-ckad-faq)
- [Certification and Confidentiality Agreement](http://training.linuxfoundation.org/go/CNCF-certification-and-confidentiality-agreement)
- [Verify Certification](https://training.linuxfoundation.org/certification/verify-certifications)
- [CKA Reseller FAQs](https://www.cncf.io/certification/expert/cka/reseller-faqs/)
- [Read: A Community Member’s Experience](https://www.cncf.io/blog/2021/07/30/success-story-preparing-for-kubernetes-certification-improves-a-platform-development-engineers-skill-set/)

During the exam you are allowed be allowed to open **one** tab apart from the browser based terminal. You can open _any_ link under the [kubernetes.io](kubernetes.io) domain. Some links that will help during the exam are;

* [https://kubernetes.io/docs/reference/kubectl/cheatsheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet)
* [https://discuss.kubernetes.io](https://discuss.kubernetes.io)
* [https://kubernetes.io/docs/home/](https://kubernetes.io/docs/home/)

If you are unsure of the spec or parameters of a yaml, always use `kubectl explain <resource>.<key>`.

## 🛠 Pre-requisites

### kubectl

- [ ] Read and practice with **kubectl Cheat Sheet** - [https://kubernetes.io/docs/reference/kubectl/cheatsheet/](https://kubernetes.io/docs/reference/kubectl/cheatsheet/) - This page is an overview of the kubectl command.

These aliases will help save the precious time you have. Use these during your studies, so you are used to them on the day.

```sh
# Needed
alias k='kubectl'

# Optional
alias kgp='kubectl get pods'
alias kgs='kubectl get svc'
alias kgc='kubectl get componentstatuses'
alias kctx='kubectl config current-context'
alias kcon='kubectl config use-context'
alias kgc='kubectl config get-context'
```

### openssl/cfssl

- [ ] Read and use **OpenSSL command cheatsheet** - [https://www.freecodecamp.org/news/openssl-command-cheatsheet-b441be1e8c4a/](https://www.freecodecamp.org/news/openssl-command-cheatsheet-b441be1e8c4a/) - When it comes to security-related tasks, like generating keys, CSRs, certificates, calculating digests, debugging TLS connections and other tasks related to PKI and HTTPS, you’d most likely end up using the OpenSSL tool.

## 📚 Study

This is a list of some resoures I used to study for the exam.

### kubernetes.io

**kubernetes.io** is the best first resource for preparation of this exam, **since in exam you are allowed to open “kubernetes.io” , so preparation from this website is going to help you in the exam also.** I am preparing using “kubernetes.io” website. 

I would suggest that you follow each and every page of this website and here are my links (until now ) on which i focused more for the exam:

- ### Administer a cluster

  - Creating a cluster with kubeadm
    - [ ] https://kubernetes.io/docs/tasks/administer-cluster/configure-upgrade-etcd/

  - Operating etcd cluster
    - [ ] https://kubernetes.io/docs/tasks/administer-cluster/configure-upgrade-etcd/

  - Using RBAC Authorization
    - [ ] https://kubernetes.io/docs/reference/access-authn-authz/rbac/

- #### UNDERSTAND PODS

  - [ ] https://kubernetes.io/docs/concepts/workloads/pods/pod/
  - [ ] https://kubernetes.io/docs/concepts/workloads/pods/init-containers/

- #### UNDERSTAND AND MANAGING CONTAINER STATE USING DEPLOYMENT

  - Replica Sets 
    - [ ] https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/
  - ReplicationController
    - [ ] https://kubernetes.io/docs/concepts/workloads/controllers/replicationcontroller/
  - Daemon Sets
    - [ ] https://kubernetes.io/docs/concepts/workloads/controllers/daemonset/
  - **Rolling Updates and Rollback**
    - [ ] https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/
  - StatefulSets
    - [ ] https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/
  - Jobs and Cronjobs
    - [ ] https://kubernetes.io/docs/concepts/workloads/controllers/jobs-run-to-completion/
    - [ ] https://kubernetes.io/docs/concepts/workloads/controllers/cron-jobs/

- #### DEEP UNDERSTANDING ABOUT SERVICES

  - [ ] Services
    - [ ] https://kubernetes.io/docs/concepts/services-networking/service/
    - [ ] https://kubernetes.io/docs/concepts/services-networking/connect-applications-service/
  - DNS for Services and Pods
    - [ ] https://kubernetes.io/docs/concepts/services-networking/dns-pod-service/
  - Ingress
    - [ ] https://kubernetes.io/docs/concepts/services-networking/ingress/

- #### DETAILED UNDERSTANDING ABOUT VOLUMES

  - Volumes and Persistent Volumes
    - [ ] https://kubernetes.io/docs/concepts/storage/volumes/
    - [ ] https://kubernetes.io/docs/concepts/storage/persistent-volumes/

  - **Config Maps**

- #### POD SCHEDULING

  - Assigning Pods to Nodes
    - https://kubernetes.io/docs/concepts/configuration/assign-pod-node/
  - Taints and Tolerations
    - https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/
  - Secrets
    - [ ] https://kubernetes.io/docs/concepts/configuration/secret/
  - Organising Cluster Access using kubeconfig files
    - [ ] https://kubernetes.io/docs/concepts/configuration/organize-cluster-access-kubeconfig/
  - Scheduler
    - [ ] https://kubernetes.io/docs/concepts/configuration/scheduler-perf-tuning/

- #### LOGGING ARCHITECTURE

  - [ ] https://kubernetes.io/docs/concepts/cluster-administration/logging/

- #### MOST IMPORTANT – LOTS OF PRACTICE AND….

  - kubectl Cheat Sheet
    - [ ] https://kubernetes.io/docs/reference/kubectl/cheatsheet/

### Read

- [ ] Read **Certified Kubernetes Administrator (CKA) Study Guide** by Benjamin Muschko - https://learning.oreilly.com/library/view/certified-kubernetes-administrator/9781098107215/ -  Exclusively on O'Reilly: Get more hands-on training and test your CKA exam readiness by working through the Certified Kubernetes Administrator (CKA) Exam Prep Labs playlist. This collection of 30 interactive labs provides hands-on training that enhances the exam prep provided by this study guide.

- [ ] Read **The Kubernetes Book** by Nigel Poulton - [THE KUBERNETES BOOK](https://nigelpoulton.com/books/)

- [ ] Read **Kubernetes: Up and Running, 3rd Edition** By Brendan Burns, Joe Beda, Kelsey Hightower, Lachlan Evenson - https://learning.oreilly.com/library/view/kubernetes-up-and/9781098110192/

#### Additional Reading

> **Kubernetes Cheat Sheet – 15 Kubectl Commands & Objects** - [https://spacelift.io/blog/kubernetes-cheat-sheet](https://spacelift.io/blog/kubernetes-cheat-sheet)

> **15 Kubernetes Best Practices Every Developer Should Know** - [https://spacelift.io/blog/kubernetes-best-practices](https://spacelift.io/blog/kubernetes-best-practices)

### Do

- [ ] Do **all** the tasks on [https://kubernetes.io/docs/tasks/](https://kubernetes.io/docs/tasks/) - This section of the Kubernetes documentation contains pages that show how to do individual tasks. A task page shows how to do a single thing, typically by giving a short sequence of steps.

- [ ] Do **kelseyhightower/kubernetes-the-hard-way** if you you have access to the [Google Cloud Platform](https://cloud.google.com/). - [https://github.com/kelseyhightower/kubernetes-the-hard-way](https://github.com/kelseyhightower/kubernetes-the-hard-way) - This tutorial walks you through setting up Kubernetes the hard way. This guide is not for people looking for a fully automated command to bring up a Kubernetes cluster.   Kubernetes The Hard Way is optimized for learning, which means taking the long route to ensure you understand each task required to bootstrap a Kubernetes cluster.

- [ ] or Do **Kubernetes The Hard Way On VirtualBox** if you want setup a local environment - [https://github.com/mmumshad/kubernetes-the-hard-way](https://github.com/mmumshad/kubernetes-the-hard-way) - This tutorial is a modified version of the original developed by [Kelsey Hightower](https://github.com/kelseyhightower/kubernetes-the-hard-way). While the original one uses GCP as the platform to deploy kubernetes, it use VirtualBox and Vagrant to deploy a cluster on a local machine. If you prefer the cloud version, refer to the original one [here](https://github.com/kelseyhightower/kubernetes-the-hard-way)

### Courses

- [ ] Do **Certified Kubernetes Administrator (CKA) with Practice Tests(Udemy)** course - [https://www.udemy.com/certified-kubernetes-administrator-with-practice-tests/](https://www.udemy.com/certified-kubernetes-administrator-with-practice-tests/) or **CKA Certification Course – Certified Kubernetes Administrator(KodeKloud)** course [https://kodekloud.com/courses/certified-kubernetes-administrator-cka/](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/) - Both courses were prepared by Mumshad Mannambeth for the Certified Kubernetes Administrators Certification with live practice tests right in your browser.

- [ ] Do **Kubernetes Deep Dive** course - [https://acloud.guru/learn/kubernetes-deep-dive](https://acloud.guru/learn/kubernetes-deep-dive) - Everything you need to know to start deploying and managing cloud-native applications on Kubernetes in the real world.


### Additional Resources

There is a google spreadsheet created by the community that compiles a lot of useful resources that can be found [here](https://bit.ly/2IdKwIc).

Some additional useful Github repositories:

-  https://github.com/stretchcloud/cka-lab-practice
-  https://github.com/walidshaari/Kubernetes-Certified-Administrator
-  https://github.com/krzko/awesome-cka
-  https://github.com/David-VTUK/CKA-StudyGuide


