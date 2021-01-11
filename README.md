# ArgoCD App of Apps Tutorial - 2048 Example Child App

## Overview

This repo is based on [alexwhen/docker-2048](https://github.com/alexwhen/docker-2048), which is in turn based on [gabrielecirulli/2048](https://github.com/gabrielecirulli/2048).

## Purpose

This repo is part of the [App of Apps overview and tutorial on Medium](https://medium.com/@dee_zero/ea4993190e7c?source=friends_link&sk=1980f3547b68251370d4223d7098f589), where we learn about the [ArgoCD App of Apps pattern](https://argoproj.github.io/argo-cd/operator-manual/cluster-bootstrapping/#app-of-apps-pattern), [Kustomized Helm](https://jfrog.com/blog/power-up-helm-charts-using-kustomize-to-manage-kubernetes-deployments/), and how to put it all together.

This type of repo would typically be created and managed by an application development team.

Repos in this tutorial:
* [argocd-app-of-apps-parent](https://github.com/d0-labs/argocd-app-of-apps-parent)
* [argocd-app-of-apps-child-2048-game](https://github.com/d0-labs/argocd-app-of-apps-child-2048-game)
* [argocd-app-of-apps-child-guestbook](https://github.com/d0-labs/argocd-app-of-apps-child-guestbook)

## Pre-Requisites

To use this example repo as part of our ArgoCD App of Apps tutorial, you need a Kubernetes cluster with the following installed:
* [ArgoCD](https://argoproj.github.io)

To find out how to install the above tools in your Kubernetes cluster, check out our [Medium blog post](https://medium.com/dzerolabs/installing-ambassador-argocd-and-tekton-on-kubernetes-540aacc983b9). It has all the gory details you need to get started!

## Build and Run Dockerfile Locally

To try building and running the Dockerfile locally yourself:

```bash
# Build
docker build -t docker-2048:1.0.0 .

# Run in interactive mode
docker run -it -p 80:8000 docker-2048:1.0.0
```

Once the Docker image is built, you can check it out at: `http://localhost`

## Tekton Pipeline & ArgoCD Application Deployments

Looking how to use Tekton and ArgoCD to build and deploy this code to your Kubernetes cluster? Head on over to [d0-labs/tekton-pipeline-example-pipeline](https://github.com/d0-labs/tekton-pipeline-example-pipeline)

