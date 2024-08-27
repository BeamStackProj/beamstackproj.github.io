+++
title = "Architecture"
description = "An overview of Beamstack's architecture"
weight = 10
+++

This guide introduces Beamstack's ecosystem and explains how it fits in the ML lifecycle. Read [the introduction guide](/docs/getting-started/introduction) to learn more about Beamstack.

## Beamstack Ecosystem

The following diagram gives an overview of the Beamstack Ecosystem and how it relates to the wider
Kubernetes and AI/ML landscapes.

<img src="./docs/getting-started/images/beam-arch.png"
  alt="An architectural overview of Beamstack on Kubernetes"
  class="mt-3 mb-3">

### How does Beamstack initilize components on a cluster?

Beamstack pulls components directly from the registry using helm and kustomize and installs them on the kubernetes cluster.

<img src="./docs/getting-started/images/initialization.png"
  alt="Cluster Initialization using Beamstack"
  class="mt-3 mb-3"
  width="900">

### How does Beamstack deploy Beam YAML pipeline's to the cluster?

Beamstack copies the Beam YAML pipeline file to the persistent volume, then the pipeline runners access the file from the persistent volume and create jobs.

<img src="./docs/getting-started/images/deploy.png"
  alt="Pipeline deployment using Beamstack"
  class="mt-3 mb-3"
  width="900">



### Beamstack Components

See the following links for more information about each Beamstack component:

- [Beamstack CLI](https://github.com/BeamStackProj/beamstack-cli) can be used for deploying and monitoring AI/ML Pipelines

- [Beamstack Custom Transforms](https://github.com/BeamStackProj/transforms) can be used for data
  tranformation.

- [Apache Beam YAML](https://beam.apache.org/documentation/sdks/yaml/) contains pipeline specifications

## Next steps

- Follow [Installing Beamstack](/docs/getting-started/installing-beamstack/) to set up your environment and install Beamstack.
