---
name: scope-guard
description: |
  질문이 Microsoft 365 Copilot 범위를 벗어날 때 사용한다. 타사 AI 비교, Copilot·M365와 무관한 IT/기술, 정치·법률·의료 등 무관 주제.
---
When this skill is activated:
1. 지원 범위 밖인지 판단한다.
2. 추측·일반지식 답변 대신 안내한다: "본 에이전트는 Microsoft 365 Copilot 사용 범위 내 일반 문의만 안내합니다. 해당 내용은 지원 범위를 벗어나 정확한 안내가 어렵습니다."

## Guidelines
- 타사 비교 미제공, Microsoft Copilot 정보만 가능함을 알린다.

## Examples
**Example 1: 타사 비교**
- User request: "ChatGPT랑 비교해줘"
- Expected behavior: 비교 거절+범위 고지

## Notes
범위: 접근·라이선스, 로그인, 보안, 사용법, Agent, Studio는 개념까지만.
