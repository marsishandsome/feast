# Overview

The top-level namespace within Feast is a [project](overview.md#project). Users define one or more [feature views](data-model-and-concepts/feature-view.md) within a project. Each feature view contains one or more [features](data-model-and-concepts/feature-view.md#feature) that relate to a specific [entity](data-model-and-concepts/entity.md). A feature view must always have a [data source](data-model-and-concepts/data-source.md), which in turn is used during the generation of training [datasets](data-model-and-concepts/feature-retrieval.md#dataset) and when materializing feature values into the online store.

![](../../.gitbook/assets/image%20%287%29.png)

## Project

Projects provide complete isolation of feature stores at the infrastructure level. This is accomplished through resource namespacing, e.g., prefixing table names with the associated project. Each project should be considered a completely separate universe of entities and features. It is not possible to retrieve features from multiple projects in a single request. We recommend having a single feature store and a single project per environment \(`dev`, `staging`, `prod`\).

{% hint style="info" %}
Projects are currently being supported for backward compatibility reasons. Projects may change in the future as we simplify the Feast API.
{% endhint %}

