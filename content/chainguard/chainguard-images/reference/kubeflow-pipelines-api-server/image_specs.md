---
title: "kubeflow-pipelines-api-server Image Variants"
type: "article"
unlisted: true
description: "Detailed information about the public kubeflow-pipelines-api-server Chainguard Image variants"
date: 2023-03-07T11:07:52+02:00
lastmod: 2023-03-07T11:07:52+02:00
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
weight: 550
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=false url="/chainguard/chainguard-images/reference/kubeflow-pipelines-api-server/" >}}
{{< tab title="Variants" active=true url="/chainguard/chainguard-images/reference/kubeflow-pipelines-api-server/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/kubeflow-pipelines-api-server/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/kubeflow-pipelines-api-server/provenance_info/" >}}
{{</ tabs >}}

This page shows detailed information about all public variants of the Chainguard **kubeflow-pipelines-api-server** Image.

## Variants Compared
The **kubeflow-pipelines-api-server** Chainguard Image currently has 2 public variants: 

- `latest-dev`
- `latest`

The table has detailed information about each of these variants.

|              | latest-dev                                                                                        | latest                                                                                            |
|--------------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Default User | `nonroot`                                                                                         | `nonroot`                                                                                         |
| Entrypoint   | not specified                                                                                     | not specified                                                                                     |
| CMD          | `/usr/bin/apiserver --config=/config --sampleconfig=/config/sample_config.json -logtostderr=true` | `/usr/bin/apiserver --config=/config --sampleconfig=/config/sample_config.json -logtostderr=true` |
| Workdir      | not specified                                                                                     | not specified                                                                                     |
| Has apk?     | yes                                                                                               | no                                                                                                |
| Has a shell? | yes                                                                                               | no                                                                                                |

Check the [tags history page](/chainguard/chainguard-images/reference/kubeflow-pipelines-api-server/tags_history/) for the full list of available tags.

## Packages Included
The table shows package distribution across variants.

|                                | latest-dev | latest |
|--------------------------------|------------|--------|
| `apk-tools`                    | X          |        |
| `bash`                         | X          |        |
| `busybox`                      | X          |        |
| `ca-certificates-bundle`       | X          | X      |
| `git`                          | X          |        |
| `glibc`                        | X          | X      |
| `glibc-locale-posix`           | X          | X      |
| `kubeflow-pipelines-apiserver` | X          | X      |
| `ld-linux`                     | X          | X      |
| `libbrotlicommon1`             | X          |        |
| `libbrotlidec1`                | X          |        |
| `libcrypt1`                    | X          |        |
| `libcrypto3`                   | X          | X      |
| `libcurl-openssl4`             | X          |        |
| `libexpat1`                    | X          |        |
| `libgcc`                       | X          | X      |
| `libnghttp2-14`                | X          |        |
| `libpcre2-8-0`                 | X          |        |
| `libssl3`                      | X          | X      |
| `libstdc++`                    | X          | X      |
| `ncurses`                      | X          |        |
| `ncurses-terminfo-base`        | X          |        |
| `openssl-config`               | X          | X      |
| `wget`                         | X          | X      |
| `wolfi-baselayout`             | X          | X      |
| `zlib`                         | X          |        |

