---
date: 2023-10-04T23:20:44Z
title: "chainctl clusters print-config"
slug: chainctl_clusters_print-config
url: /chainguard/chainctl/chainctl-docs/chainctl_clusters_print-config/
draft: false
tags: ["chainctl", "Reference", "Product"]
images: []
type: "article"
toc: true
---
## chainctl clusters print-config

Print the tenant configuration in YAML.

```
chainctl clusters print-config [--profiles=PROFILE1,PROFILE2,...] [--opt=KEY=VALUE,KEY=VALUE...]
```

### Options

```
  -h, --help                   help for print-config
      --opt strings            extra key=value pairs to define enforcer profile options
      --profiles stringArray   The names of Chainguard profiles to install into the cluster.
```

### Options inherited from parent commands

```
      --api string                   The url of the Chainguard platform API. (default "https://console-api.enforce.dev")
      --audience string              The Chainguard token audience to request. (default "https://console-api.enforce.dev")
      --config string                A specific chainctl config file.
      --console string               The url of the Chainguard platform Console. (default "https://console.enforce.dev")
      --issuer string                The url of the Chainguard STS endpoint. (default "https://issuer.enforce.dev")
  -o, --output string                Output format. One of: ["", "table", "tree", "json", "id", "wide"]
      --timestamp-authority string   The url of the Chainguard Timestamp Authority endpoint. (default "https://tsa.enforce.dev")
  -v, --v int                        Set the log verbosity level.
```

### SEE ALSO

* [chainctl clusters](/chainguard/chainctl/chainctl-docs/chainctl_clusters/)	 - Cluster related commands for the Chainguard platform.

