---
title: "fluent-bit Image Variants"
type: "article"
unlisted: true
description: "Detailed information about the public fluent-bit Chainguard Image variants"
date: 2023-03-07T11:07:52+02:00
lastmod: 2023-03-07T11:07:52+02:00
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
weight: 550
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=false url="/chainguard/chainguard-images/reference/fluent-bit/" >}}
{{< tab title="Variants" active=true url="/chainguard/chainguard-images/reference/fluent-bit/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/fluent-bit/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/fluent-bit/provenance_info/" >}}
{{</ tabs >}}

This page shows detailed information about all public variants of the Chainguard **fluent-bit** Image.

## Variants Compared
The **fluent-bit** Chainguard Image currently has one public variant: 

- `latest`

The table has detailed information about each of these variants.

|              | latest                               |
|--------------|--------------------------------------|
| Default User | `nonroot`                            |
| Entrypoint   | `/usr/bin/fluent-bit`                |
| CMD          | `-c /fluent-bit/etc/fluent-bit.conf` |
| Workdir      | not specified                        |
| Has apk?     | no                                   |
| Has a shell? | no                                   |

Check the [tags history page](/chainguard/chainguard-images/reference/fluent-bit/tags_history/) for the full list of available tags.

## Packages Included
The table shows package distribution across variants.

|                          | latest |
|--------------------------|--------|
| `ca-certificates-bundle` | X      |
| `fluent-bit`             | X      |
| `glibc`                  | X      |
| `glibc-locale-posix`     | X      |
| `ld-linux`               | X      |
| `libcap`                 | X      |
| `libcrypto3`             | X      |
| `libgcc`                 | X      |
| `libpq-11`               | X      |
| `libssl3`                | X      |
| `libsystemd`             | X      |
| `openssl-config`         | X      |
| `wolfi-baselayout`       | X      |
| `yaml`                   | X      |
| `zlib`                   | X      |

