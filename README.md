# Infrastructure Management via ACM

This repository includes a set of objects required to implement an Openshift multi-cluster and multi-environment configuration approach based on Red Hat Advantage Cluster Management (ACM).

In terms of the repo organization, the following list includes the most important information about the different folders:

* acm -> This folder includes ACM object required to configure the Hub instance
* des/pre/pro -> These folders include an ArgoCD ApplicationSet and an ACM Placement per environment that defines the Helm Chart and some values files hosted in a specific Git repository for setting up the Openshift clusters in every environment (Create quotas, network policies, etc)

## Prerequisites

It is necessary to keep into account the following prerequisites:

- Openshift 4.18+
- Red Hat Red Hat Advantage Cluster Management (ACM) Installed
- Red Hat GitOps Operator Installed in the Hub and managed clusters

## Setting Up

In order to start working with ACM and define the required minimum ArgoCD applications, execute the following command:

```$bash
oc apply -f acm/*
```

## Author

Asier Cidon @RedHat