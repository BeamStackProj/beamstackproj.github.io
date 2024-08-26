+++
title =  "Deploy a simple beam pipeline with beamstack"
description = "How to deploy a simple beam pipeline with beamstack"
weight = 50
type = "docs"
+++

{{< tabpane text=true left=true >}}
  {{% tab header="YAML" lang="en" %}}
  ```go
  pipeline:
    type: chain
    transforms:
        - type: Create
          config:
              elements: [1, 5, 2, 7, 3, 8, 10]
        - type: LogForTesting
  ```
  {{% /tab %}}
{{< /tabpane >}}


<div style="position: relative; padding-bottom: 64.5933014354067%; height: 0;"><iframe src="https://www.loom.com/embed/86f019b88a0a451fb9052fd97fb5ab9c?sid=56c569f5-72be-4fd1-ab33-164d905d7630" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

<br>
