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
> Regardless of your environment, setup or operating system, Beamstack takes your Beam YAML file with defined specifications and resources, processes it and allows a kubernetes cluster to be spun up with given specifications. 

> The Kubernetes operator runners such as Flink operator, Spark operator etc take up the job and spins up a worker pool that contain beamstack harnesses. 

> Beamstack enusres that your data is migrated from your local device or remote machine to the pipeline. 

> Once the pipeline has been deployed, users can up the flink UI and Grafana dashboard to visually inspect the pipeline and derive insights about it's performance.

## What are Standalone Beamstack Components?

The Beamstack ecosystem is composed of multiple open-source projects such as [Apache Beam](https://beam.apache.org/) and [Kubernetes](https://kubernetes.io/) that address different aspects
of the ML lifecycle. Many of these projects are designed to be usable both within the Beamstack Platform and independently.

## The Beamstack mission

Our goal is to make the deployment of AI/ML Pipelines effortless and time efficienct. Beamstack extends already existing features of kubernetes: 

- Easy, repeatable, portable deployments on a diverse infrastructure
  (for example, experimenting on a laptop, then moving to an on-premises
  cluster or to the cloud)
- Deploying and managing loosely-coupled microservices
- Scaling based on demand

Because ML practitioners use a diverse set of tools, one of the key goals is to
customize the stack based on user requirements (within reason) and let the
system take care of the "boring stuff".

## History

Beamstack is a new open-source tool that is still currently under development. We welcome you to [Join us](https://discord.gg/fYNnNVaEFK) as we build the next generation of deployment mechanisms.

## Roadmaps

To see what's coming up in future versions of Beamstack, refer to the [Beamstack roadmap](https://github.com/BeamStackProj/beamstack-cli).

## Getting involved

There are many ways to contribute to Beamstack, and we welcome contributions!

Read the [contributor's guide](/docs/about/contributing/) to get started on the code, and learn about the community on the [community page](/docs/about/community/).

## Next Steps

- Follow [the installation guide](/docs/getting-started/installing-beamstack) install Beamstack and begin easy pipeline deployments.
