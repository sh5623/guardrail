# guardrail

<div align="right">
  <a href="README.ko.md"><img src="https://img.shields.io/badge/lang-한국어-lightgrey?style=flat-square" alt="한국어"/></a>
  <a href="README.md"><img src="https://img.shields.io/badge/lang-English-blue?style=flat-square" alt="English"/></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-green?style=flat-square" alt="MIT License"/></a>
</div>

> One Claude Code marketplace, all three plugins.

`guardrail` is a thin marketplace repo — it holds no plugin code of its own. It just lists three plugins that already live in their own repos, so you can add one marketplace instead of three:

| Plugin | What it does | Repo |
|---|---|---|
| **fe-rail** | Frontend harness — automates the spec → build → review → PR cycle for Next.js App Router / Vite SPA + TypeScript, Tailwind v3/v4, shadcn/ui | [sh5623/fe-rail](https://github.com/sh5623/fe-rail) |
| **self-improvement** | Evidence-gated convention repair loop, plus a budget/archive system that keeps rule docs from growing without bound. Stack-agnostic | [sh5623/self-improvement](https://github.com/sh5623/self-improvement) |
| **parallel-worktree** | Orchestrate parallel subagents in isolated git worktrees — bootstrap, dispatch, harvest, and the failure modes a green gate cannot see. Skill-only, stack-agnostic | [sh5623/parallel-worktree](https://github.com/sh5623/parallel-worktree) |

Each plugin keeps its own version, release history, and README in its own repo — `guardrail` only points to them. Installing directly from any of `sh5623/fe-rail`, `sh5623/self-improvement`, or `sh5623/parallel-worktree` still works if you only need one.

## Install

```bash
claude

/plugin marketplace add sh5623/guardrail
/plugin install fe-rail@guardrail
/plugin install self-improvement@guardrail
/plugin install parallel-worktree@guardrail
/reload-plugins
```

Install only one plugin by running just its `/plugin install` line.

## Updating

```bash
/plugin marketplace update guardrail
/reload-plugins
```

This refreshes the marketplace listing. Each plugin still updates independently — see its own repo for update notes (`self-improvement` in particular requires an `si-init` re-run after updates; see its README).

## License

[MIT](LICENSE) © 2026 이승호
