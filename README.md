# JAEYONG TEST HELM CHART

[nevido](https://github.com/nevido/helm-chart) is a web-based application that
enables the search and discovery of charts from multiple Helm Chart
repositories. It is the codebase that powers the [Helm
Hub](https://github.com/helm/hub) project.

## TL;DR;

```console
$ helm repo add nevido https://nevido.github.io/helm-chart
$ helm install name/name
```

## Introduction

This chart bootstraps a [nevido](https://github.com/nevido/helm-chart) deployment on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Prerequisites

### [Nginx Ingress controller](https://github.com/kubernetes/ingress)

To avoid issues with Cross-Origin Resource Sharing, the Monocular chart sets up an Ingress resource to serve the frontend and the API on the same domain. This is used to route requests made to `<host>:<port>/` to the frontend pods, and `<host>:<port>/api` to the backend pods.

## Installing the Chart

First, ensure you have added the Monocular chart repository:

```console
$ helm repo add monocular https://helm.github.io/monocular
```

To install the chart with the release name `my-release`:

```console
$ helm install --name my-release nevido
```

The command deploys Monocular on the Kubernetes cluster in the default configuration. The [configuration](#configuration) section lists the parameters that can be configured during installation.

> **Tip**: List all releases using `helm list`

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
$ helm delete my-release
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration

See the [values](values.yaml) for the full list of configurable values.

