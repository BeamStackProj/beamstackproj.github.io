---
title: Examples
# date: 2017-01-05
description: >
  This page contains some of the examples and use cases of beamstack.
---

{{% pageinfo %}}
To run the examples displayed here on your local computer, ensure beamstack in installed properly.
{{% /pageinfo %}}

{{< alert  title="Warning" color="warning">}}Ensure you have a cluster running before running any command{{< /alert >}}

### Initialize a Kubernetes Cluster with Beamstack & Monitoring tools

``` go
beamstack init -m
```

### Get the current kubernetes cluster context and profile info

``` go
beamstack info
```

### Display the name, status and age of a cluster

``` go
beamstack info cluster
```

### Create a runner cluster

``` go
beamstack create [runner-cluster] [cluster-name]
```

### Open runner UI

``` go
beamstack open [runner] [runner-cluster-name]
```

### Open Grafana dashboard

``` go
beamstack open dashboard
```

### Deploy a pipeline

``` go
beamstack deploy pipeline [FILE] [flags]
```

### Create a vector store

``` go
beamstack create vector-store --type=elasticsearch
```
