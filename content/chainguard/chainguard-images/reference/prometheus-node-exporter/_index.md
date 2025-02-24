---
title: "Image Overview: prometheus-node-exporter"
linktitle: "prometheus-node-exporter"
type: "article"
layout: "single"
description: "Overview: prometheus-node-exporter Chainguard Image"
date: 2022-11-01T11:07:52+02:00
lastmod: 2022-11-01T11:07:52+02:00
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
menu:
  docs:
    parent: "images-reference"
weight: 500
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=true url="/chainguard/chainguard-images/reference/prometheus-node-exporter/" >}}
{{< tab title="Variants" active=false url="/chainguard/chainguard-images/reference/prometheus-node-exporter/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/prometheus-node-exporter/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/prometheus-node-exporter/provenance_info/" >}}
{{</ tabs >}}



Minimalist Wolfi-based Prometheus Node Exporter image for exporting node metrics.

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/prometheus-node-exporter:latest
```

## Usage

The easiest way to install the Prometheus Node Exporter is to use the Helm chart.

Get the digest of the image, and then install the chart:

```bash
$ helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
$ helm repo update
$ helm install prom-node-exporter prometheus-community/prometheus-node-exporter \
 --set image.registry=cgr.dev \
 --set image.repository=chainguard/prometheus-node-exporter \
 --set image.digest=[DIGEST]
```

For more detail, please refer to the [Node Exporter documentation](https://github.com/prometheus/node_exporter).

