---
title: "Image Overview: kubernetes-ingress-defaultbackend"
linktitle: "kubernetes-ingress-defaultbackend"
type: "article"
layout: "single"
description: "Overview: kubernetes-ingress-defaultbackend Chainguard Image"
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
{{< tab title="Overview" active=true url="/chainguard/chainguard-images/reference/kubernetes-ingress-defaultbackend/" >}}
{{< tab title="Variants" active=false url="/chainguard/chainguard-images/reference/kubernetes-ingress-defaultbackend/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/kubernetes-ingress-defaultbackend/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/kubernetes-ingress-defaultbackend/provenance_info/" >}}
{{</ tabs >}}



Minimal image that acts as a drop-in replacement for the `registry.k8s.io/defaultbackend` image. Used in some ingresses like https://github.com/kubernetes/ingress-gce and https://github.com/kubernetes/ingress-nginx

The image runs as `non-root`.

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/kubernetes-ingress-defaultbackend:latest
```

You can run it with the standard deployment using nginx-ingress with something like:

```
helm install <RELEASE_NAME> ingress-nginx/ingress-nginx \
  --set defaultBackend.image.registry=cgr.dev/chainguard \
  --set defaultBackend.image.image=kubernetes-ingress-defaultbackend \
  --set defaultBackend.image.tag=latest
```

