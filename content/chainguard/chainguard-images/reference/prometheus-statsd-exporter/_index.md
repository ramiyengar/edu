---
title: "Image Overview: prometheus-statsd-exporter"
linktitle: "prometheus-statsd-exporter"
type: "article"
layout: "single"
description: "Overview: prometheus-statsd-exporter Chainguard Image"
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
{{< tab title="Overview" active=true url="/chainguard/chainguard-images/reference/prometheus-statsd-exporter/" >}}
{{< tab title="Variants" active=false url="/chainguard/chainguard-images/reference/prometheus-statsd-exporter/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/prometheus-statsd-exporter/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/prometheus-statsd-exporter/provenance_info/" >}}
{{</ tabs >}}



Minimalist Wolfi-based Prometheus StatsD Exporter image for exporting metrics to StatsD.

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/prometheus-statsd-exporter:latest
```

## Usage

The easiest way to install the Prometheus StatsD Exporter is to use the Helm chart.

```bash
$ helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
$ helm repo update
$ helm install prom-statsd-exporter prometheus-community/prometheus-statsd-exporter \
 --set image.repository=cgr.dev/chainguard/prometheus-statsd-exporter --set image.tag=latest
```

For more detail, please refer to the [StatsD Exporter documentation](https://github.com/prometheus/statsd_exporter).

