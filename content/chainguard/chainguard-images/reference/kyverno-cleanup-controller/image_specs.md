---
title: "kyverno-cleanup-controller Image Variants"
type: "article"
unlisted: true
description: "Detailed information about the public kyverno-cleanup-controller Chainguard Image variants"
date: 2023-03-07T11:07:52+02:00
lastmod: 2023-03-07T11:07:52+02:00
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
weight: 550
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=false url="/chainguard/chainguard-images/reference/kyverno-cleanup-controller/" >}}
{{< tab title="Variants" active=true url="/chainguard/chainguard-images/reference/kyverno-cleanup-controller/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/kyverno-cleanup-controller/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/kyverno-cleanup-controller/provenance_info/" >}}
{{</ tabs >}}

This page shows detailed information about all public variants of the Chainguard **kyverno-cleanup-controller** Image.

## Variants Compared
The **kyverno-cleanup-controller** Chainguard Image currently has one public variant: 

- `latest`

The table has detailed information about each of these variants.

|              | latest                        |
|--------------|-------------------------------|
| Default User | `nonroot`                     |
| Entrypoint   | `/usr/bin/cleanup-controller` |
| CMD          | `help`                        |
| Workdir      | not specified                 |
| Has apk?     | no                            |
| Has a shell? | no                            |

Check the [tags history page](/chainguard/chainguard-images/reference/kyverno-cleanup-controller/tags_history/) for the full list of available tags.

## Packages Included
The table shows package distribution across variants.

|                              | latest |
|------------------------------|--------|
| `ca-certificates-bundle`     | X      |
| `kubectl-1.28`               | X      |
| `kubectl-latest`             | X      |
| `kyverno-cleanup-controller` | X      |
| `wolfi-baselayout`           | X      |

