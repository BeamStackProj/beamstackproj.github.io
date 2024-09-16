---
date: 2024-09-16
title: Launching Beamstack at the Beamsummit conference, Google Campus, Sunnyvale CA.
linkTitle: Launching Beamstack
description: >
  Beamstack is an open-source framework currently under development, aimed at facilitating the 
  deployment of Machine Learning and Gen AI workflow pipelines with Apache Beam on Kubernetes. 
author: Olufunbi Babalola
resources:
  - src: "**.{png,jpg,svg}"
    title: "Image #:counter"
---

## Introduction
The goal of Beam Summit is to connect a community of professionals around the world who use, contribute, and are learning Apache Beam. 
This annual conference provides space to share use cases, performance, and resource optimizations, discuss pain points, and 
talk about the benefits of implementing Apache Beam in organizations. The event aims to bring together the Apache Beam community to 
discuss the project’s status, its technical advances, and its future.

Contents are focused on sharing:
- New use cases from companies using Apache Beam.
- Community-driven talks.
- Technical deep dives.
- In-depth workshops.

At the beamsummit conference, Beamstack was introduced and launched as an open-source framework aimed at facilitating the deployment of Machine Learning and GenAI workflow pipelines with Apache Beam on Kubernetes. Beamstack was introduced by MavenCode ML Engineers and Product managers in 2 separeate presentations. 

- The first presentation titled **"Beamstack: An Open source Framework for running Machine Learning Pipelines with Apache Beam"** delivered by **Olufunbi Babalola** and **Mathew Fait** introduced beamstack, the product roadmap, how to use beamstack and a call for participation.
- The second presentation titled **"A Low Code Structured Approach to Deploying Apache Beam ML Workloads on Kubernetes using Beamstack"** delivered by **Charles Adetiloye** and **Nate Salawe** discussed a low code structured approach to deploying apache beam ML workloads on Kubernetes using Beamstack

## Beamstack: An Open source Framework for running Machine Learning Pipelines with Apache Beam

### Agenda
- Overview of Beamstack
- Why do you need Beamstack?
- Beamstack Architecture
- How to use Beamstack
- Product Roadmap
- Call for Participation


### Overview of Beamstack
Beamstack is an open-source framework currently under development, aimed at facilitating the deployment of Machine Learning 
and GenAI workflow pipelines with Apache Beam on Kubernetes. Beamstack provides a robust Command Line Interface (CLI) that can potentially reduce 
pipeline deployment complexity and timelines drastically. It also possesses great monitoring and visualization features.  

### Why do you need Beamstack?
{{< imgproc why Fit "2542x842" >}}
{{< /imgproc >}}
- **Configurable Deployment Environment**: With minimal steps you can setup Beamstack on your local minikube, bare metal or cloud infrastructure
- **Ease of Deployment with Beam Low-code YAML**: Beamstack adopts a low-code approach towards pipeline deployment which makes the process easier and faster
- **Composable and Reusable Pipeline Components**: Reusable pipeline components designed for easy composition and customization, enabling efficient workflow creation and deployment.
- **Collaborative Setup for Development Teams**: Beamstack’s modular architecture facilitates collaborative setup’s for various technical teams within an organization

### Beamstack Architecure
{{< imgproc beamstack Fit "2362x1046" >}}
{{< /imgproc >}}

### How to use Beamstack
{{< imgproc install Fit "2424x980" >}}
{{< /imgproc >}}

- **Install the binary**: Install the beamstack binary from the releases section on the beamstack Github repository
- **Configre the target environment**: Beamstack initializes your target kubernetes cluster with the necessary components
- **Select YAML package to deploy**: Run and deploy your YAML pipeline by running the beamstack deploy command
- **Monitor your running jobs**: Open the grafana dashboard or runner UI to observe your running jobs

### Beamstack Roadmap
Feature Implementation
{{< imgproc roadmap Fit "2998x1018" >}}
{{< /imgproc >}}

Tasks Breakdown
{{< imgproc tasks Fit "2308x988" >}}
{{< /imgproc >}}


### Call for Participation
We would like to encourage you to join our discord channel to engage with fellow beamstack developers, become a contributor and drive adoption of beamstack

<a href="https://discord.gg/fYNnNVaEFK">
  <button class="btn btn-primary py-2 px-5 mb-3">Click to join:<br><b>Beamstack Discord</b></button>
</a>

## A Low Code Structured Approach to Deploying Apache Beam ML Workloads on Kubernetes using Beamstack

### Agenda
- Overview of Beamstack
- Architecture Overview
- Key Features of Beamstack
- Beamstack Use Cases / Demos
- Future Roadmap


### Overview of Beamstack
Beamstack is an open-source framework currently under development, aimed at facilitating the deployment of Machine Learning 
and GenAI workflow pipelines with Apache Beam on Kubernetes. Beamstack provides a robust Command Line Interface (CLI) that can potentially reduce 
pipeline deployment complexity and timelines drastically. It also possesses great monitoring and visualization features.  

{{< imgproc overview Fit "2248x930" >}}
{{< /imgproc >}}

### Architecture Overview
{{< imgproc layout Fit "2466x1086" >}}
{{< /imgproc >}}

### Key Features of Beamstack
{{< imgproc features Fit "2558x850" >}}
{{< /imgproc >}}

### Beamstack Use Cases & Demos
Beamstack can currently used in the following ways
{{< imgproc usecases Fit "2154x698" >}}
{{< /imgproc >}}

Example Use Case: Creating Text Embedding + Saving it to Vector Database
{{< imgproc inference Fit "2390x1106" >}}
{{< /imgproc >}}

Beamstack Demo
<iframe src="https://drive.google.com/file/d/1YkgvWHE1xM8zxxCtHq9PMF7C2Ky2ndhE/preview" width="1080" height="480" allow="autoplay"></iframe> 

### Future Roadmap
{{< imgproc future Fit "2034x1228" >}}
{{< /imgproc >}}

