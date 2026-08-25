# guardrail

<div align="right">
  <a href="README.ko.md"><img src="https://img.shields.io/badge/lang-한국어-blue?style=flat-square" alt="한국어"/></a>
  <a href="README.md"><img src="https://img.shields.io/badge/lang-English-lightgrey?style=flat-square" alt="English"/></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-green?style=flat-square" alt="MIT License"/></a>
</div>

> 마켓 하나로 플러그인 셋 다.

`guardrail`은 자체 코드가 없는 얇은 마켓 레포다. 각자 자기 레포에 이미 존재하는 플러그인 세 개를 목록으로만 가리켜서, 마켓을 세 번 add 하지 않고 한 번만 add 하면 되게 만든다.

| 플러그인 | 하는 일 | 레포 |
|---|---|---|
| **fe-rail** | 프론트엔드 하네스 — Next.js App Router / Vite SPA + TypeScript, Tailwind v3/v4, shadcn/ui 대상 spec → build → review → PR 사이클 자동화 | [sh5623/fe-rail](https://github.com/sh5623/fe-rail) |
| **self-improvement** | 근거 기반(evidence-gated) 컨벤션 수선 루프 + 룰 문서가 무한정 커지지 않도록 하는 예산/아카이브 체계. 스택 무관 | [sh5623/self-improvement](https://github.com/sh5623/self-improvement) |
| **parallel-worktree** | 격리 git 워크트리에서 서브에이전트를 병렬로 돌리고 수확하는 파이프라인 — 부트스트랩·투입·수확, 그리고 게이트가 초록인 채로 실패하는 지점들. 스킬 단독, 스택 무관 | [sh5623/parallel-worktree](https://github.com/sh5623/parallel-worktree) |

각 플러그인은 버전·릴리스·README를 자기 레포에서 그대로 유지한다 — `guardrail`은 그걸 가리키기만 한다. 하나만 필요하면 `sh5623/fe-rail`·`sh5623/self-improvement`·`sh5623/parallel-worktree` 중 해당 레포로 직접 설치해도 여전히 동작한다.

## 설치

```bash
claude

/plugin marketplace add sh5623/guardrail
/plugin install fe-rail@guardrail
/plugin install self-improvement@guardrail
/plugin install parallel-worktree@guardrail
/reload-plugins
```

하나만 쓰려면 해당 `/plugin install` 줄만 실행하면 된다.

## 업데이트

```bash
/plugin marketplace update guardrail
/reload-plugins
```

마켓 목록만 갱신한다. 각 플러그인 자체 업데이트는 독립적이다 — 특히 `self-improvement`는 업데이트 후 `si-init` 재실행이 필요하니 해당 레포 README를 참고할 것.

## License

[MIT](LICENSE) © 2026 이승호
