+++
title = "Introduction"
description = "An introduction to Beamstack"
weight = 1
+++

## What is Beamstack?

Beamstack is an open-source framework currently under development, aimed at facilitating the deployment of Machine Learning and GenAI workflow pipelines with Apache Beam on Kubernetes. 

Beamstack provides a robust Command Line Interface (CLI) that can potentially reduce pipeline deployment complexity and timelines drastically. It also possesses great monitoring and visualization features. Beamstack makes AI/ML on Kubernetes simple, portable, and scalable.

<img src="/docs/getting-started/images/architecture-light.png"
  alt="Beamstack overview"
  class="mt-3 mb-3">

Read the [architecture overview](/docs/getting-started/architecture/) to learn about the Beamstack ecosystem
and to see how Beamstack components fit in ML lifecycle.

## Why Beamstack?
Deploying machine learning and GenAI workflows should be easy. By extension, managing those workflows should be easy as well, beamstack offers a solution that streamlines the deployment process of complex workflows. It is an open-source tool, easy to understand, and versatile. 

## How it works
> Beamstack quickly sets up your Kubernetes cluster with all necessary resources, like operators, CRDs, and monitoring, so you can run Beam workflows, regardless of your environment.

> Beamstack analyzes your Beam YAML file and automatically migrates any referenced data from your host device to a persistent storage volume on your Kubernetes cluster, aiding in pipeline prototyping.

> Beamstack then runs the pipeline in your already initialized cluster.

>  Beamstack provides helper functions to view pipelines on a Grafana dashboard and access the pipeline runner UI, like Flink UI.

## The Beamstack mission

Our goal is to make the deployment of AI/ML Pipelines effortless and time efficienct. Beamstack extends already existing features of kubernetes: 

- Easy, repeatable, portable deployments on a diverse infrastructure
  (for example, experimenting on a laptop, then moving to an on-premises
  cluster or to the cloud)
- Scaling based on demand

## History

Beamstack is a new open-source tool that is still currently under development. We welcome you to [Join us](https://discord.gg/fYNnNVaEFK) as we build the next generation of deployment mechanisms.

## Roadmaps

To see what's coming up in future versions of Beamstack, refer to the [Beamstack roadmap](https://github.com/BeamStackProj/beamstack-cli).

## Getting involved

There are many ways to contribute to Beamstack, and we welcome contributions!

Read the [contributor's guide](/docs/about/contributing/) to get started on the code, and learn about the community on the [community page](/docs/about/community/).

## Next Steps

- Follow [the installation guide](/docs/getting-started/installing-beamstack) install Beamstack and begin easy pipeline deployments.
