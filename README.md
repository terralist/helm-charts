# Terralist Charts

Installs [Terralist](https://github.com/terralist/terralist), A truly private Terraform registry.

# Goal

This repo contains helm charts the Terralist community developed to help deploy Terralist on Kubernetes cluster.

It leverages the bitnami [common-library chart](https://github.com/bitnami/charts/tree/da4aaf376e800760fd5ada2b07e3c85c7c8ddd95/bitnami/common) to make configuration as easy as possible. 

# Installation

```
$ helm install --create-namespace --namespace terralist terralist oci://ghcr.io/terralist/helm-charts/terralist -f values.yaml
```

You should not copy the full values.yaml from this repository. Only set the values that you want to override.

There are a few things that you are required to configure in your values.yaml before installing the chart:
* ...
* ...
* ...

# Configuration

The Terralist chart is highly customizable. You can see a detailed documentation
of all possible changes within the `charts/terralist/values.yaml` file.

## Chart architecture 

This chart uses the [common library](https://github.com/bitnami/charts/tree/da4aaf376e800760fd5ada2b07e3c85c7c8ddd95/bitnami/common) from [Bitnami](https://bitnami.com/). You can freely add more top level keys to be applied to all the components, please reference [the common library's values.yaml](https://github.com/bitnami/charts/blob/main/bitnami/common/values.yaml) to see what keys are available.

## Uninstalling the Chart

To see the currently installed Terralist chart:

```console
helm ls --namespace terralist
```

To uninstall/delete the `terralist` chart:

```console
helm delete --namespace terralist terralist
```

The command removes all the Kubernetes components associated with the chart and deletes the release.