---
date: 2023-10-04T23:20:44Z
title: "chainctl auth status"
slug: chainctl_auth_status
url: /chainguard/chainctl/chainctl-docs/chainctl_auth_status/
draft: false
tags: ["chainctl", "Reference", "Product"]
images: []
type: "article"
toc: true
---
## chainctl auth status

Inspect the local Chainguard Token.

```
chainctl auth status [--output table|json] [flags]
```

### Options

```
  -h, --help                    help for status
      --identity-token string   Use an explicit passed identity token or token path.
      --quick                   Whether to perform quick offline token checks (vs. calling the Validate API).
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

* [chainctl auth](/chainguard/chainctl/chainctl-docs/chainctl_auth/)	 - Auth related commands for the Chainguard platform.

