---
title: "M13. 설계서 완성"
nav_order: 14
---

# 나만의 에이전트 설계서 완성 ⭐
{: .no_toc }

| 시간 | 소요 | 수강생 역할 |
|:-----|:-----|:-----------|
| 17:30 | 20분 | 🟢 설계서 완성 |

## 목차
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 이 모듈에서 배우는 것

- M4에서 만든 설계서를 **오늘 배운 내용으로 업그레이드**
- 빈칸이 **구체적인 계획**으로 채워지는 것 확인
- "내일 당장 에이전트를 만들 수 있다"는 **자신감** 획득

---

## 아침의 씨앗 → 오후의 꽃

M4에서 설계서를 만들었을 때, 에이전트·지침·지식·Topic이 뭔지 잘 몰랐습니다.

**지금은 다릅니다.** 아침엔 몰랐던 단어들이 지금은 다 보입니다.

{: .highlight }
> 이 설계서를 꺼내서 다시 보세요. 아침과 지금, 얼마나 달라졌는지 확인해 보세요.

---

## 설계서 업그레이드 — 6가지 포인트

아래 항목을 확인하면서 설계서를 구체화하세요.

| 항목 | 아침 (M4) | 지금 업그레이드 | 연결 모듈 |
|:-----|:---------|:--------------|:---------|
| **에이전트 이름** | "○○ 도우미" | 그대로 or 더 구체적으로 | M3 |
| **역할/범위** | 막연한 설명 | 역할·범위·태도·원칙 4요소 반영 | M5 |
| **지식 소스** | "회사 문서" | 어떤 파일을 업로드할지 구체화 | M6 |
| **FAQ 시나리오** | 없거나 1개 | 주요 질문 3개 + 예상 답변 | M7 |
| **배포 채널** | 미정 | Teams / @호출 / 웹 명시 | M8 |
| **자동화 연결** | 없음 | 어떤 Flow가 필요한지 1~2줄 | M9 |

---

## 실습: Copilot으로 설계서 완성

Copilot에게 아래 프롬프트를 입력하세요:

<details markdown="1">
<summary><strong>프롬프트 (클릭해서 펼치기)</strong></summary>

```
아래는 내가 만들고 싶은 에이전트 설계서 초안이야.
오늘 학습한 내용을 바탕으로 더 구체적으로 보완해줘:

[여기에 아침 설계서 내용 붙여넣기]

다음 항목을 채워줘:
- 지침의 역할/범위/태도/원칙
- 업로드할 지식 파일 3개
- 필요한 Flow 1~2개
- 배포 채널
- FAQ 시나리오 3개
```

</details>

{: .tip }
> 직접 작성해도 좋고, Copilot의 도움을 받아도 좋습니다. 중요한 건 **구체적으로 채우는 것**입니다.

---

## Before vs After 비교

### Before (M4)

<details markdown="1">
<summary><strong>Before 설계서 (클릭해서 펼치기)</strong></summary>

```
에이전트 이름: HR 도우미
목적: 직원 질문에 답변
지식 소스: 회사 문서들
배포: Teams
```

</details>

### After (M13)

<details markdown="1">
<summary><strong>After 설계서 (클릭해서 펼치기)</strong></summary>

```
에이전트 이름: HR 도우미
목적: 신입사원 온보딩부터 경비처리까지 모든 HR 질문에 즉시 자동 답변

지침:
  역할: HR팀을 대신하는 친절한 도우미
  범위: 복리후생 + 연차 규정 + 경비처리
  태도: 한국어 존칭, 핵심 먼저, 200자 이내
  원칙: 모르는 질문 → HR팀 연결

지식 소스:
  - FAQ.docx (Q&A 형식)
  - 복리후생가이드.docx
  - 담당자정보.xlsx

배포: Teams + @호출
Flow: RequestByEmail (문의접수 메일 자동 전달)
FAQ: "연차 며칠?", "경비처리 어떻게?", "복지포인트 사용처?"
```

</details>

{: .important }
> 이 설계서로 **내일 당장 에이전트를 만들 수 있습니다.**

---

## 다음 단계: 이 설계서로 만들기

설계서가 완성되었다면, 아래 순서로 실제 에이전트를 만들 수 있습니다.

| 순서 | 할 일 | 참고 모듈 |
|:-----|:------|:---------|
| 1 | Copilot Studio에서 에이전트 생성 | M3 |
| 2 | 지침(채용공고) 입력 | M5 |
| 3 | 지식 파일 업로드 | M6 |
| 4 | Topic + STRICT RULES 설정 | M7 |
| 5 | Teams에 배포 | M8 |
| 6 | Flow 연결 (필요시) | M9 |
| 7 | 대화기록 설정 (선택) | M10 |

---

## 핵심 정리

1. 아침의 설계서(M4)가 오늘의 배움으로 **완성된 실행 계획**이 되었습니다
2. 이 설계서 하나로 **내일 당장 에이전트를 만들 수 있습니다**
3. 아이디어를 말하면 Copilot이 설계하고, **여러분이 만듭니다**

---

## FAQ

| 질문 | 답변 |
|:-----|:-----|
| 설계서대로 실제로 만들 수 있나요? | 네! M3~M10 단계를 따라가면 됩니다. 설계서가 로드맵입니다. |
| 설계서를 더 다듬고 싶은데 시간이 부족해요 | 큰 그림만 잡으세요. 내일 Copilot과 함께 다듬으면 됩니다. |
| 만들다 막히면 어떻게 하나요? | MS Learn 문서, Copilot Studio 커뮤니티, 그리고 이 교안의 참조 링크를 활용하세요. |
| 회사에서 Copilot Studio를 못 쓰면요? | 관리자에게 라이선스를 문의하세요. 설계서의 개념은 다른 도구에도 적용 가능합니다. |

---

## 참조 자료

| 자료 | 링크 |
|:-----|:-----|
| Copilot Studio 공식 문서 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/) |
| MS Learn 학습 경로 | [learn.microsoft.com](https://learn.microsoft.com/training/paths/work-power-virtual-agents/) |
| Copilot Studio 커뮤니티 | [community.powerplatform.com](https://community.powerplatform.com/galleries/communitycontent/?v=copilot-studio) |
| Power Automate 커뮤니티 | [community.powerplatform.com](https://community.powerplatform.com/galleries/communitycontent/?v=power-automate) |

---

{: .highlight }
> **"문과생이 에이전트를 만드는 시대 — 오늘 그 첫 번째 사람이 되셨습니다."**

[← 처음으로 돌아가기]({{ site.baseurl }}/)
