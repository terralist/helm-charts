# Terralist Charts

Installs [Terralist](https://github.com/terralist/terralist), A truly private Terraform registry.

# Goal

This repo contains helm charts the terralist community developed to help deploy terralist on Kubernetes cluster.

It leverages the bjw-s [common-library chart](https://github.com/bjw-s-labs/helm-charts/tree/923ef40a39520979c98f354ea23963ee54f54433/charts/library/common) to make configuration as easy as possible. 

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

This chart uses the [common library](https://github.com/bjw-s-labs/helm-charts/tree/923ef40a39520979c98f354ea23963ee54f54433/charts/library/common). You can freely add more top level keys to be applied to all the components, please reference [the common library's values.yaml](https://github.com/bjw-s-labs/helm-charts/blob/923ef40a39520979c98f354ea23963ee54f54433/charts/library/common/values.yaml) to see what keys are available.

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