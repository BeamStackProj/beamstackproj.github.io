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



<br>
