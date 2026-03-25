---
title: "M8. 배포"
nav_order: 9
---

# 게시·배포 — Teams + Copilot
{: .no_toc }

| 시간 | 소요 | 수강생 역할 |
|:-----|:-----|:-----------|
| 15:10 | 20분 | 🟢 직접 실습 |

## 목차
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 이 모듈에서 배우는 것

- Copilot Studio에서 에이전트를 **게시(Publish)**
- **Teams에 배포**하고 직접 대화
- M365 Copilot에서 **@호출**로 에이전트 사용
- **재게시** 개념 이해

---

## 배포 채널 4가지

| 채널 | 추천 상황 | 오늘 실습 |
|:-----|:---------|:---------|
| **Microsoft Teams** | 팀 내부용·협업 도구 연동 | ✅ 실습 |
| SharePoint 페이지 | 사내 포털에 삽입 | 소개만 |
| **M365 Copilot @호출** | 빠르게 사용 (인컨텍스트) | ✅ 실습 |
| 웹사이트 임베드 | 외부 고객 대상 | 소개만 |

---

## 실습 ①: 게시(Publish)

### Step-by-Step

1. Copilot Studio → 에이전트 편집 화면
2. 우측 상단 **"게시(Publish)"** 클릭
3. 게시 확인 대화상자 → **"게시"** 클릭
4. 게시 완료 (1~2분 소요)

{: .highlight }
> 게시 = 에이전트의 **배포판**을 만드는 것입니다. 게시하지 않으면 테스트 패널에서만 사용 가능합니다.

---

## 실습 ②: Teams 배포

### Step-by-Step

1. Copilot Studio → 좌측 메뉴 **"채널"**
2. **"Microsoft Teams"** 클릭
3. **"Teams에서 사용"** 활성화
4. 설정 저장
5. **Teams 앱** 열기 → 에이전트 이름으로 검색
6. 에이전트와 **대화 시작!**

---

## 실습 ③: @호출 테스트

1. M365 Copilot 채팅 열기 (Teams 또는 브라우저)
2. 입력: `@에이전트이름 복지포인트 사용처 알려줘`
3. 에이전트가 답변하는 것 확인

{: .tip }
> @호출은 M2에서 배운 **인컨텍스트** 방식입니다. 다른 업무 중 빠르게 질문할 때 편합니다.

---

## 배포 후 공유

에이전트를 동료와 공유하려면:
- 에이전트 **설정 → 공유** → 동료 이메일 입력
- 또는 관리자가 **조직 전체에 배포**

---

## 재게시

{: .important }
> **배포는 1회성이 아닙니다.** 에이전트를 수정할 때마다 다시 게시해야 Teams에 반영됩니다.

M9에서 Flow를 추가한 뒤 → **다시 게시 버튼** 누르기  
→ Teams의 에이전트에 새 기능이 즉시 반영됩니다.

---

## 핵심 정리

1. **게시** = 에이전트의 배포판 만들기
2. **Teams 배포** = 팀원이 바로 사용 가능
3. **@호출** = Copilot 채팅에서 빠르게 질문
4. **수정 후에는 반드시 재게시**

---

## FAQ

| 질문 | 답변 |
|:-----|:-----|
| Teams에서 에이전트가 안 보여요 | 게시 후 1~3분 소요됩니다. 재검색해 보세요. |
| @호출이 안 됩니다 | 게시 여부 확인, Copilot 채널 활성화 확인, 관리자 정책 확인이 필요합니다. |
| 다른 팀원도 바로 쓸 수 있나요? | 공유 설정에서 추가하거나 조직 전체 배포가 가능합니다. |
| 배포 취소 가능한가요? | 채널에서 비활성화하거나 에이전트를 비게시 상태로 전환할 수 있습니다. |

---

## 참조 자료

| 자료 | 링크 |
|:-----|:-----|
| 에이전트 게시 기본 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/publication-fundamentals-publish-channels) |
| Teams에 에이전트 배포 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/publication-add-bot-to-microsoft-teams) |
| M365 Copilot 에이전트 연결 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-365-copilot/extensibility/) |
| 에이전트 공유 및 협업 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/admin-share-bots) |

---

다음 모듈: [M9. Flow + 메일 전달](m09-flow-card)
