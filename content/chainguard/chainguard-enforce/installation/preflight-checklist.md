---
title: "Preflight Checklist for Chainguard Enforce"
linktitle: "Preflight Checklist"
type: "article"
date: 2023-07-07T05:56:52-07:00
lastmod: 2023-07-07T05:56:52-07:00
draft: false
tags: ["Enforce", "chainctl", "Product"]
images: []
menu:
  docs:
    parent: "installation"
toc: true
weight: 005
# This resource contains some inline CSS to remove bullets on this page (showing only checkboxes)
---
<style type="text/css" rel="stylesheet">
* { list-style: none; }
</style>

There are a few things you need to have in place in order to install Chainguard Enforce. However, there's more than one offering of Chainguard Enforce and there are multiple different ways to install them. Because each installation method has its own set of prerequisites, it's important to be clear on exactly what you need to have in place before you install Chainguard Enforce.

This document is intended to serve as a quick reference outlining the various components you need in order to install Chainguard Enforce under each currently-available method. It starts with a general list of prerequisites across the various installation methods. It then provides a brief overview of every installation method and highlights the prerequisites needed for each.

Note that, in addition to the prerequisites listed here, there are [additional requirements for the Chainguard Enforce Agent](/chainguard/chainguard-enforce/reference/installation-requirements/) as well as [network requirements](/chainguard/chainguard-enforce/reference/network-requirements/) one should consider when installing Chainguard Enforce.


## General Installation Checklist

The following is a list of prerequisites required across all the different installation methods available for Chainguard Enforce. 

- [x] &nbsp;&nbsp;Every installation method requires you to have access to Chainguard Enforce. Sign up using [this inquiry form](https://www.chainguard.dev/contact?utm_source=docs) if you don't already have access.
- [X] &nbsp;&nbsp;Most installation methods require you to have `chainctl` installed. You can achieve this by following our [How to Install `chainctl` tutorial](https://edu.chainguard.dev/chainguard/chainguard-enforce/how-to-install-chainctl/).
- [x] &nbsp;&nbsp;Some installation methods require you to have a special tool like [Terraform](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli#install-terraform) or [Helm](https://helm.sh/docs/intro/install/) installed on your computer or system. 
- [x] &nbsp;&nbsp;The installation methods that involve Terraform also require you to [set up a cloud account association](/chainguard/chainguard-enforce/cloud-account-associations/) between Chainguard Enforce and your GCP or AWS account.
- [x] &nbsp;&nbsp;If you're installing the Chainguard Enforce Agent, it's important to know whether the resources you're installing it onto are public or private as the installation methods differ slightly for each.

Not every installation method requires each prerequisite in this list. The reason for this is that we provide two different connection methods for Chainguard Enforce. The method each cluster uses to connect to Enforce is determined at installation, and there are multiple installation procedures for both connection methods which likewise have their own unique prerequisites.

We currently provide two ways to connect your clusters to Chainguard Enforce: with the [Chainguard Enforce Agent](/chainguard/chainguard-enforce/enforce-overview/#the-chainguard-enforce-agent) and through [Agentless connections](/chainguard/chainguard-enforce/how-to-connect-kubernetes-clusters/#agentless-connections).


## Agent or Agentless?

An important decision you need to make before installation is whether you want your resources to connect to Chainguard Enforce using the Chainguard Agent or Agentless connections.

A software agent is a program that performs certain actions on behalf of a user. A software agent has the authority to make decisions on its own and doesn’t necessarily require user input. Accordingly, the Chainguard Enforce Agent is able to analyze a given cluster and enforce any policies you’ve applied to the cluster without manual human oversight.

Instead of installing the Agent directly on your cluster, you can allow a remote Agent — managed by Chainguard — to access your cloud account resources on your behalf. A SaaS offering of Enforce, Agentless connections can be useful since they don’t consume any cluster resources. Because they’re managed by Chainguard, issues can often be addressed more quickly than clusters using agentful connections. Additionally, Agentless connections allow for read-only access to your clusters, which some users may find desirable. Be aware that Agentless connections are limited to public GKE and EKS clusters and Google Cloud Run, AWS ECS, and AWS AppRunner projects.

The following table outlines some of the key differences between the Agent and Agentless connections.

|   | Chainguard Agent | Agentless Connections |
|:--- | ---: | ---:|
| **Managed by...** | User-managed | SaaS managed by Chainguard  |
| **Consumes cluster resources?** | Yes | No  |
| **Compatible with both `chainctl` and the Chainguard Console?** | Yes | Yes  |
| **Compatible with private resources?** | Yes | No |
| **Compatible with public resources?** | Yes | Yes <br> (limited to certain GCP and AWS resources) |

The remainder of this document will walk through the various installation methods available for the Chainguard Enforce Agent and Agentless connections. It will highlight each method's prerequisites and include links to appropriate documentation along the way.


## Installing the Chainguard Enforce Agent

When installing the Chainguard Enforce Agent, you can do so either interactively or declaratively. 

### Installing the Agent interactively

To install Chainguard Enforce interactively, you need to have been granted access and to have `chainctl` installed. You must also know whether the resources where you're installing Enforce are public or private. Private resources require the `--private` option when installing with `chainctl`.

You need the following to [**install Chainguard Enforce declaratively with `chainctl`**](/chainguard/chainguard-enforce/installation/alternative-installation-methods/#install-with-chainctl).
- [ ] &nbsp;&nbsp;[Access to Chainguard Enforce](https://www.chainguard.dev/contact?utm_source=docs).
- [ ] &nbsp;&nbsp;[`chainctl` installed on your local machine](https://edu.chainguard.dev/chainguard/chainguard-enforce/how-to-install-chainctl/).
- [ ] &nbsp;&nbsp;You should also know whether the resources you're installing it onto are public or private.


### Installing the Agent declaratively

There are currently two methods available for installing the Chainguard Enforce Agent declaratively: using Helm or using YAML. As with installing interactively, you must also take additional steps if you are using a declarative method to [install the Chainguard Enforce Agent on a private cluster](/chainguard/chainguard-enforce/installation/alternative-installation-methods/#additional-authentication-for-private-clusters). 

To install Chainguard Enforce declaratively [with YAML](/chainguard/chainguard-enforce/installation/alternative-installation-methods/#declarative-option-1--install-with-yaml) or [with Helm](/chainguard/chainguard-enforce/installation/alternative-installation-methods/#declarative-option-2--install-with-a-helm-chart), you must have the following.
- [ ] &nbsp;&nbsp;[Access to Chainguard Enforce](https://www.chainguard.dev/contact?utm_source=docs).
- [ ] &nbsp;&nbsp;[`chainctl` installed on your local machine](https://edu.chainguard.dev/chainguard/chainguard-enforce/how-to-install-chainctl/).
- [ ] &nbsp;&nbsp;You should also know whether the resources you're installing it onto are public or private.
- [ ] &nbsp;&nbsp;**For Helm installations**, you will need to have [the Helm CLI installed](https://helm.sh/docs/intro/install/).


## Installing Chainguard Enforce in Agentless mode

Instead of installing the Chainguard Enforce Agent directly on your cluster, you can allow a remote Agent — managed by Chainguard — to access your cloud account resources on your behalf. Known as “Agentless connections” these can be useful since they don’t consume any cluster resources and, because they’re managed by Chainguard, issues can often be addressed more quickly than clusters using agentful connections.

There are two main approaches you can take to install Agentless Chainguard Enforce. You can use [Chainguard Enforce's Discovery feature](/chainguard/chainguard-enforce/chainguard-enforce-discovery-onboarding/) (either through the Console, with `chainctl`, or with Terraform) to discover your cloud resources and install Chainguard Enforce in Agentless mode onto them. You can alternatively set up a cloud account association between Chainguard Enforce and your GCP or AWS account and then install Enforce in Agentless mode manually.

### Installing Agentless with Discovery using the Console

You can use the Discovery feature in the Chainguard Enforce Console to find resources in your associated GCP and AWS cloud accounts. You'll then have the option to enroll any available resources into Agentless Chainguard Enforce.

Aside from needing a web browser to access the Console, there's only one prerequisite to [installing Agentless using Discovery in the Console](/chainguard/chainguard-enforce/chainguard-enforce-discovery-onboarding/#option-1--chainguard-enforce-console).
- [ ] &nbsp;&nbsp;[Access to Chainguard Enforce](https://www.chainguard.dev/contact?utm_source=docs).

### Installing Agentless using `chainctl` or Terraform

Instead of using Enforce's Discovery feature in the Chainguard Console, you can use it over the command line to find your cloud resources and install Chainguard Enforce in Agentless mode. Alternatively, if you know which of your GCP or AWS resources you want to install Agentless Chainguard Enforce onto, you can skip using the Discovery feature and install it directly with `chainctl`.

The procedures for installing Agentless Chainguard Enforce with Discovery using [`chainctl`](/chainguard/chainguard-enforce/chainguard-enforce-discovery-onboarding/#option-2--chainctl-cluster-discover) and [Terraform](/chainguard/chainguard-enforce/chainguard-enforce-discovery-onboarding/#option-3--chainguard-terraform-provider), as well as [using `chainctl` to install it manually](/chainguard/chainguard-enforce/how-to-connect-kubernetes-clusters/#agentless-connections), all have the same prerequisites.

- [ ] &nbsp;&nbsp;[Access to Chainguard Enforce](https://www.chainguard.dev/contact?utm_source=docs).
- [ ] &nbsp;&nbsp;[`chainctl` installed on your local machine](https://edu.chainguard.dev/chainguard/chainguard-enforce/how-to-install-chainctl/).
- [ ] &nbsp;&nbsp;[Terraform installed on your local machine](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli#install-terraform).
- [ ] &nbsp;&nbsp;A [cloud account associations](/chainguard/chainguard-enforce/cloud-account-associations/) configured between Chainguard Enforce and your GCP or AWS account.


## Learn more

If you'd like to get Chainguard Enforce up and running to test it and see how it works, we encourage you to follow our guide on [Getting Started with Chainguard Enforce](/chainguard-enforce/chainguard-enforce-user-onboarding/) guide. This tutorial involves installing `chainctl`, preparing an example Kubernetes cluster with `kind`, and setting up and enforcing a policy.