+++
title = "Architecture"
description = "An overview of Beamstack's architecture"
weight = 10
+++

This guide introduces Beamstack's ecosystem and explains how it fits in the beam pipeline job lifecycle. Read [the introduction guide](/docs/getting-started/introduction) to learn more about Beamstack.

## Beamstack Ecosystem

The following diagram gives an overview of the Beamstack Ecosystem and how it relates to the wider Kubernetes and AI/ML landscapes.

<img src="{{< param prefixURL >}}/docs/getting-started/images/beam-arch.png"
  alt="An architectural overview of Beamstack on Kubernetes"
  class="mt-3 mb-3">  

## Core Components  
Beamstack architecture consists of three main components:

<details>
  <summary><b>Beam Runners Kubernetes Operators:</b></summary>
  <ul>
    <li>Flink, Spark, Samza, etc.</li>
  </ul>
</details>

<details>
  <summary><b>Worker Pool:</b></summary>
  <ul>
    <li>Beamstack Harness for running the pipeline jobs</li>
  </ul>
</details>

<details>
  <summary><b>Monitoring Stack:</b></summary>
  <ul>
    <li>Grafana, Prometheus for monitoring and visualizations</li>
  </ul>
</details> 

### Beam Runners Kubernetes Operators  
Beamstack supports multiple Beam runners, each orchestrated through its respective Kubernetes Operator. These operators provide the necessary logic to manage the lifecycle of data processing jobs running on different engines, including:  

<details>
  <summary><b>Apache Flink Operator:</b></summary>
  <ul>
    <li>Manages job submission, execution, scaling, and failure recovery for Flink-based data processing jobs.</li>
  </ul>
</details>

<details>
  <summary><b>Apache Spark Operator:</b></summary>
  <ul>
    <li>Handles Spark jobs by submitting them to the Kubernetes cluster and manages their lifecycle (scheduling, scaling, resource management).</li>
  </ul>
</details>

<details>
  <summary><b>Samza Operator:</b></summary>
  <ul>
    <li>Orchestrates the deployment and execution of Samza jobs in Kubernetes.</li>
  </ul>
</details>
</p>
</p>

Each operator configures the required Custom Resource Definitions (CRDs) that define how jobs and resources are represented within the Kubernetes cluster. These CRDs include specifications for job parameters, execution environment configurations, and resource allocation (e.g., CPU, memory).  

<details>
  <summary><b>Job submission and orchestration:</b></summary>
  <ul>
    <li>Runners submit Beam pipelines as Kubernetes Jobs via custom CRDs.</li>
  </ul>
</details>

<details>
  <summary><b>Scaling and resource management:</b></summary>
  <ul>
    <li>Dynamic scaling based on workload and predefined policies.</li>
  </ul>
</details>

<details>
  <summary><b>Failure handling and recovery:</b></summary>
  <ul>
    <li>Automated failure detection and job recovery mechanisms.</li>
  </ul>
</details>  
</p>
</p>

**Deployment**:  
The operators are deployed as part of the Beamstack installation. Helm charts or Kustomize templates are used to deploy the operators, ensuring ease of configuration across different clusters.  

---

### Worker Pool: Beamstack Harness
The `Beamstack Harness` is responsible for managing the pool of workers that execute the stages of Beam pipelines. These workers are dynamically provisioned within the Kubernetes cluster based on the resource requirements of the pipeline.  

**Key Responsibilities**:
<details>
  <summary><b>Worker Pod Management:</b></summary>
  <ul>
    <li>Beamstack launches worker pods in the Kubernetes cluster based on the requirements of the submitted Beam pipeline.</li>
  </ul>
</details>

<details>
  <summary><b>Task Scheduling:</b></summary>
  <ul>
    <li>Each worker processes a subset of tasks within a Beam pipeline. The Harness ensures task scheduling and load balancing across worker pods.</li>
  </ul>
</details>

<details>
  <summary><b>Resource Utilization Optimization:</b></summary>
  <ul>
    <li>Beamstack ensures that worker resources (CPU, memory) are optimized for the workload, automatically adjusting the pool size based on job demand.</li>
  </ul>
</details>  
</p>
</p>

### Monitoring Stack: Grafana, Prometheus  
To ensure robust observability, Beamstack integrates with a monitoring stack that includes `Prometheus` for metrics collection and `Grafana` for visualization.  

**Prometheus**:
<details>
  <summary><b>Metrics collection:</b></summary>
  <ul>
    <li>Prometheus scrapes metrics from Kubernetes components, the Beam Runners, and worker pods. This includes data such as job execution times, resource utilization (CPU, memory), pod health, and pipeline performance.</li>
  </ul>
</details>  
</p>
</p>

**Grafana**:
<details>
  <summary><b>Visualization:</b></summary>
  <ul>
    <li>Grafana provides dashboards that visualize real-time metrics and historical trends. Pre-built dashboards are included to track pipeline performance, resource utilization, and overall cluster health.</li>
  </ul>
</details>

<details>
  <summary><b>Custom Dashboards:</b></summary>
  <ul>
    <li>Beamstack integrates custom Grafana dashboards to monitor specific aspects of their Beam pipelines or Kubernetes cluster.</li>
  </ul>
</details>  
</p>
</p>

## Initialization and Configuration
When Beamstack is initialized on a target Kubernetes cluster, it sets up the necessary components to manage Beam pipelines. The initialization involves the following steps:

### Custom Resource Definitions (CRDs)
The Beam Runners Operators configure their own CRDs within the cluster. These CRDs define the resources for job submission and execution.

### Kubernetes Operators Deployment
Beamstack deploys Kubernetes Operators for Flink, Spark, Samza, etc. These operators are responsible for managing the jobs for each runner, ensuring that the correct resources are allocated, and that jobs are scheduled and monitored.

### Monitoring Stack Setup
Beamstack installs Prometheus and Grafana into the cluster. Prometheus is configured to scrape metrics from the Beam Runners and worker pods, while Grafana is set up with pre-configured dashboards to visualize pipeline and cluster metrics.

### Cluster Resource Configuration
Beamstack configures resource allocation strategies for running Beam pipelines efficiently. This includes setting up Horizontal Pod Autoscalers (HPAs), setting resource quotas, and configuring node selectors or taints/tolerations to ensure that workloads are assigned to the appropriate nodes.

## Detailed Flow of Pipeline Execution
<details>
  <summary><b>Pipeline Submission:</b></summary>
  <ul>
    <li>A Beam pipeline YAML configuration is submitted via beamstack CLI</li>
  </ul>
</details>

<details>
  <summary><b>Job Submission:</b></summary>
  <ul>
    <li>The Beam pipeline job is submitted via the chosen Beam Runner (e.g., Flink, Spark, Samza).</li>
  </ul>
</details>
<details>
  <summary><b>Job Scheduling:</b></summary>
  <ul>
    <li>The Kubernetes Operator for the respective runner handles job scheduling, ensuring the required resources (worker pods) are available.</li>
  </ul>
</details>

<details>
  <summary><b>Worker Pool Execution:</b></summary>
  <ul>
    <li>The Beamstack Harness manages the worker pods responsible for executing tasks within the pipeline. Tasks are distributed among the worker pods, and execution is monitored.</li>
  </ul>
</details> 

<details>
  <summary><b>Metrics Collection:</b></summary>
  <ul>
    <li>Prometheus scrapes real-time metrics from the worker pods and operators. These metrics are displayed in Grafana for monitoring.</li>
  </ul>
</details>

<details>
  <summary><b>Job Completion:</b></summary>
  <ul>
    <li>Upon successful completion, the worker pods are terminated, and the results are stored or pushed to the configured data sinks.</li>
  </ul>
</details>
</p>
</p>

## Next steps

- Follow [Installing Beamstack](/docs/getting-started/installing-beamstack/) to set up your environment and install Beamstack.
