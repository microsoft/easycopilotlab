---
title: "M8. 게시와 공유"
nav_order: 9
---

# 게시(Publish) + 공유 — Copilot에서 에이전트 사용
{: .no_toc }

| 시간 | 소요 | 수강생 역할 |
|:-----|:-----|:-----------|
| 15:15 | 20분 | 🟢 직접 실습 |

## 목차
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 이 모듈에서 배우는 것

- Copilot Studio에서 에이전트를 **게시(Publish)**
- **M365 Copilot에서 에이전트 사용** — 몰입형(전용 화면) + @호출
- 다른 사람과 사용할 수 있도록 **공유(Share)**
- **재게시** 개념 이해

---

## 용어 먼저 정리

| 용어 | 뜻 |
|:-----|:---|
| **게시(Publish)** | Copilot Studio의 최신 변경사항을 사용 채널에 반영할 준비를 하는 단계 |
| **사용 채널** | M365 Copilot, Teams, 웹사이트처럼 실제로 에이전트를 쓰는 위치 |
| **공유(Share)** | 특정 동료나 조직이 그 에이전트를 사용할 수 있게 권한을 주는 단계 |

---

## 사용 채널 4가지

| 채널 | 추천 상황 | 오늘 실습 |
|:-----|:---------|:---------|
| **M365 Copilot (몰입형)** | 에이전트 전용 화면에서 집중 대화 | ✅ 실습 |
| **M365 Copilot (@호출)** | 빠르게 사용 (인컨텍스트) | ✅ 실습 |
| Microsoft Teams | 팀 내부용·협업 도구 연동 | 소개만 |
| 웹사이트 임베드 | 외부 고객 대상 | 소개만 |

---

## 실습 ①: 게시(Publish)

### Step-by-Step

1. Copilot Studio → 에이전트 편집 화면
2. 우측 상단 **"게시(Publish)"** 클릭
3. 게시 확인 대화상자 → **"게시"** 클릭
4. 게시 완료 (1~2분 소요)

{: .highlight }
> 게시 = 최신 변경사항을 **실사용 버전**에 반영하는 단계입니다. 게시하지 않으면 테스트 패널에서만 확인됩니다.

---

## 실습 ②: Copilot에서 에이전트 사용 (몰입형)

M2에서 배운 **몰입형** 방식입니다. 에이전트 전용 화면에서 1:1로 대화합니다.

### Step-by-Step

1. [M365 Copilot](https://copilot.microsoft.com) 접속 (또는 Teams Copilot)
2. 에이전트 목록에서 **만든 에이전트 이름 클릭**
3. 에이전트 전용 화면이 열림
4. 질문 입력: **"복지포인트 사용처 알려줘"**
5. 에이전트가 답변하는 것 확인! 🎉

{: .tip }
> 몰입형은 에이전트와 **집중 대화**할 때 적합합니다. 여러 질문을 연속으로 하거나 깊이 있는 상담이 필요할 때 사용하세요.

---

## 실습 ③: @호출 테스트 (인컨텍스트)

M2에서 배운 **인컨텍스트** 방식입니다. 다른 업무 중 빠르게 질문할 때 편합니다.

1. M365 Copilot 채팅 열기 (Teams 또는 브라우저)
2. 입력: `@에이전트이름 복지포인트 사용처 알려줘`
3. 에이전트가 답변하는 것 확인

---

## 게시 후 공유

에이전트를 동료와 공유하려면:
- 에이전트 **설정 → 공유** → 동료 이메일 입력
- 또는 관리자가 **조직 전체 사용 정책**으로 노출

---

## 재게시

{: .important }
> **게시는 1회성이 아닙니다.** 에이전트를 수정할 때마다 다시 게시해야 Copilot에 반영됩니다.

M9~M10에서 Flow를 추가한 뒤 → **다시 게시 버튼** 누르기  
→ Copilot의 에이전트에 새 기능이 즉시 반영됩니다.

---

## 핵심 정리

1. **게시** = 최신 버전을 사용 채널에 반영하는 단계
2. **몰입형** = Copilot에서 에이전트 이름 클릭 → 전용 화면에서 집중 대화
3. **@호출** = Copilot 채팅에서 빠르게 질문
4. **공유** = 다른 사람이 쓸 수 있도록 권한을 주는 단계
5. **수정 후에는 반드시 재게시**

---

## FAQ

| 질문 | 답변 |
|:-----|:-----|
| Copilot에서 에이전트가 안 보여요 | 게시 후 1~3분 소요됩니다. 새로고침 후 다시 확인해 보세요. |
| @호출이 안 됩니다 | 게시 여부 확인, Copilot 채널 활성화 확인, 관리자 정책 확인이 필요합니다. |
| 다른 팀원도 바로 쓸 수 있나요? | 공유 설정에서 추가하거나 관리자 정책으로 조직 전체에 노출할 수 있습니다. |
| 게시를 되돌릴 수 있나요? | 채널에서 비활성화하거나 에이전트를 비게시 상태로 전환할 수 있습니다. |

---

## 참조 자료

| 자료 | 링크 |
|:-----|:-----|
| 에이전트 게시 기본 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/publication-fundamentals-publish-channels) |
| Teams에 에이전트 배포 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/publication-add-bot-to-microsoft-teams) |
| M365 Copilot 에이전트 연결 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-365-copilot/extensibility/) |
| 에이전트 공유 및 협업 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/admin-share-bots) |

---

다음 모듈: [M9. Flow 만들기](m09-flow-create)
