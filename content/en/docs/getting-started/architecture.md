+++
title = "Architecture"
description = "An overview of Beamstack's architecture"
weight = 10
+++

This guide introduces Beamstack's ecosystem and explains how it fits in the ML lifecycle.

Read [the introduction guide](/docs/getting-started/introduction) to learn more about Beamstack.

## Beamstack Ecosystem

The following diagram gives an overview of the Beamstack Ecosystem and how it relates to the wider
Kubernetes and AI/ML landscapes.

<img src="/docs/getting-started/images/architecture-light.png"
  alt="An architectural overview of Beamstack on Kubernetes"
  class="mt-3 mb-3">

Beamstack builds on [Kubernetes](https://kubernetes.io/) as a system for
deploying, scaling, and managing AI/ML infrastructure.

## Introducing the ML Lifecycle

When you develop and deploy an AI application, the ML lifecycle typically consists of
several stages. Developing an ML system is an iterative process.
You need to evaluate the output of various stages of the ML lifecycle, and apply
changes to the model and parameters when necessary to ensure the model keeps
producing the results you need.

The following diagram shows the ML lifecycle stages in sequence:

<img src="/docs/getting-started/images/ml-lifecycle.drawio.svg"
  alt="ML Lifecycle"
  class="mt-3 mb-3">

Looking at the stages in more detail:

- In the _Data Preparation_ step you ingest raw data, perform feature engineering to extract ML
  features for the offline feature store, and prepare training data for model development.
  Usually, this step is associated with data processing tools such as Spark, Dask, Flink, or Ray.

- In the _Model Development_ step you choose an ML framework, develop your model architecture and
  explore the existing pre-trained models for fine-tuning like BERT or Llama.

- In the _Model Optimization_ step you can optimize your model hyperparameters and optimize your
  model with various AutoML algorithms such as neural architecture search and model compression.
  During model optimization you can store ML metadata in the _Model Registry_.

- In the _Model Training_ step you train or fine-tune your model on the large-scale
  compute environment. You should use a distributed training if single GPU can't handle your
  model size. The results of the model training is the trained model artifact that you
  can store in the _Model Registry_.

- In the _Model Serving_ step you serve your model artifact for online or batch inference. Your
  model may perform predictive or generative AI tasks depending on the use-case. During the model
  serving step you may use an online feature store to extract features. You monitor the model
  performance, and feed the results into your previous steps in the ML lifecycle.

### Beamstack Components

See the following links for more information about each Beamstack component:

- [Beamstack CLI](https://github.com/BeamStackProj/beamstack-cli) can be used for deploying and monitoring AI/ML Pipelines

- [Beamstack Custom Transforms](https://github.com/BeamStackProj/transforms) can be used for data
  tranformation.

- [Apache Beam YAML](https://beam.apache.org/documentation/sdks/yaml/) is used to define resources to be implemented

## Next steps

- Follow [Installing Beamstack](/docs/getting-started/installing-beamstack/) to set up your environment and install Beamstack.
