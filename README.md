### Introduction

This repo is an example of various Helm patterns used with Argo CD based on the excellent article by Trevor Royer found here:

https://developers.redhat.com/articles/2023/05/25/3-patterns-deploying-helm-charts-argocd#3_patterns_for_helm_charts

The examples here leverage an existing Helm chart found here:

https://github.com/gnunn-gitops/product-catalog-chart

The four patterns covered in this repo are:

1. Application directly consuming Helm chart from repo
2. Application consuming helm chart from git repo, in this example we will use it as an umbrella chart.
3. Application consuming helm chart via kustomize
4. Application consuming helm chart via the new Multi-Source feature (Tech Preview)

### Usage

All applications have an `application.yaml` file that can be run into an Argo CD instance, however the
namespaces are hardcode for `gitops-demo` for where Argo CD is installed and `gitops-demo-target` for
where the application is deployed. You will likely need to fork this repo to change the namespaces
for something that works for you.
