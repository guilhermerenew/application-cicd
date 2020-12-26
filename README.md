## What is Argo Workflows?
Argo Workflows is an open source container-native workflow engine for orchestrating parallel jobs on Kubernetes. Argo Workflows is implemented as a Kubernetes CRD (Custom Resource Definition).

* Define workflows where each step in the workflow is a container.
* Model multi-step workflows as a sequence of tasks or capture the dependencies between tasks using a directed acyclic graph (DAG).
* Easily run compute intensive jobs for machine learning or data processing in a fraction of the time using Argo Workflows on Kubernetes.
* Run CI/CD pipelines natively on Kubernetes without configuring complex software development products.

### Why Argo CD?
Argo CD is a declarative, GitOps continuous delivery tool for Kubernetes. \
Application definitions, configurations, and environments should be declarative and version controlled. Application deployment and lifecycle management should be automated, auditable, and easy to understand.

#### Core Concepts 
Let's assume you're familiar with core Git, Docker, Kubernetes, Continuous Delivery, and GitOps concepts.

- **Application** A group of Kubernetes resources as defined by a manifest. This is a Custom Resource Definition (CRD).
- **Application source type** Which Tool is used to build the application.
- **Target State** The desired state of an application, as represented by files in a Git repository.
- **Live state** The live state of that application. What pods etc are deployed.
- **Sync status** Whether or not the live state matches the target state. Is the deployed application the same as Git says it should be?
- **Sync** The process of making an application move to its target state. E.g. by applying changes to a Kubernetes cluster.
- **Sync operation status** Whether or not a sync succeeded.
- **Refresh** Compare the latest code in Git with the live state. Figure out what is different.
- **Health** The health of the application, is it running correctly? Can it serve requests?
- **Tool** A tool to create manifests from a directory of files. E.g. Kustomize or Ksonnet. See Application Source Type.
- **Configuration management tool** See **Tool**.
- **Configuration management plugin** A custom tool. 

Argo is a [Cloud Native Computing Foundation (CNCF)](https://cncf.io/) hosted project.

![CNCF Image](images/cncf.png)
