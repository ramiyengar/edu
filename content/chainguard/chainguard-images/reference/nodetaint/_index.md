---
title: "Image Overview: nodetaint"
linktitle: "nodetaint"
type: "article"
layout: "single"
description: "Overview: nodetaint Chainguard Image"
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
{{< tab title="Overview" active=true url="/chainguard/chainguard-images/reference/nodetaint/" >}}
{{< tab title="Variants" active=false url="/chainguard/chainguard-images/reference/nodetaint/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/nodetaint/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/nodetaint/provenance_info/" >}}
{{</ tabs >}}



Minimal [nodetaint](https://github.com/wish/nodetaint) container image.

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/nodetaint
```

## Usage

To install on you Kubernetes, you can use the `Helm`:

```shell
git clone https://github.com/wish/nodetaint && cd nodetaint

helm install nodetaint ./chart \
  --namespace nodetaint \
  --create-namespace \
  --set image.registry=${IMAGE_REGISTRY} \
  --set image.repository=${IMAGE_REPOSITORY} \
  --set image.tag=${IMAGE_TAG}
```

