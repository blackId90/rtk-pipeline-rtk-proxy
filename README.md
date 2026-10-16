# rtk pipeline · rtk:proxy

**23% of command output removed** — self-reported by the author's own rtk, measured on their traffic. rtk verifies nothing.

## Install

```
rtk pipeline add github:blackId90/rtk-pipeline-rtk-proxy
```

rtk shows this pipeline's rules and asks before anything installs, and pins the install to a commit. A pipeline can rewrite the commands your agent runs, filter and replace what it reads, and send content to any upstream it declares — review the rules and install only what you trust. RTK does not review or endorse shared pipelines; the author is responsible for this repo, and you are responsible for what you install.

## What it does

- **before shell** — rewrite -> rtk
- **proxy tool result** — compress [ansi, progress, dedup]
- **proxy cache** — compress [cache-align]

## Measured impact

| lever | activity | reduction |
|-------|----------|-----------|
| command filtering (rtk git/npm/…) | 8716 commands | `██░░░░░░░░` **23%** removed |

_Estimates (≈ bytes/4): ratios reliable, absolutes approximate. Percentages travel across setups; token counts and costs do not._

## user pipeline.toml

```toml
schema_version = 1

[pipeline]
extends = "rtk:proxy"
```

Measured by [rtk](https://github.com/rtk-ai/rtk) v1.0.1 on 2026-10-17.

Install this pipeline: `rtk pipeline add <url-of-this-card>`
