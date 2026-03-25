---
title: "M7. Topic + 변수"
nav_order: 8
---

# 대본(Topic) + 포스트잇(변수)
{: .no_toc }

| 시간 | 소요 | 수강생 역할 |
|:-----|:-----|:-----------|
| 14:25 | 30분 | 🟡 복붙 + 확인 |

## 목차
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 이 모듈에서 배우는 것

- **Topic = 대본** 비유 이해
- **변수 = 포스트잇** 비유 이해
- FAQ Topic + Contact Topic **2개 구현** (복붙 실습)
- 지침에 **STRICT RULES** 추가하여 Topic 호출 조건 설정

---

## Topic = 대본

Topic은 특정 상황에서 에이전트가 **어떻게 행동할지 정해놓은 대본**입니다.

생성형 오케스트레이터가 사용자의 질문을 보고, 상황에 맞는 **대본을 자동으로 선택**해서 실행합니다.

---

## 변수 = 포스트잇

변수는 대화 중 필요한 정보를 **메모해 두는 포스트잇**입니다.  
나중에 다른 Topic이나 Flow에서 꺼내 씁니다.

```
사용자: "경비처리 담당자 알려줘"
     ↓
Topic: "담당자 찾기 대본 실행"
     ↓
📝 포스트잇: [담당자: 홍길동 / 연락처: 010-1234]
     ↓
사용자: "아까 찾은 담당자한테 문의 넣어줘"
     ↓
Flow: 포스트잇의 정보를 사용해서 실행
```

### 글로벌 변수 vs 일반 변수

| 구분 | 유지 범위 | 비유 |
|:-----|:---------|:-----|
| **글로벌 변수** | 모든 대본에서 공유 | 가슴에 붙인 포스트잇 |
| 일반 변수 | 해당 대본 안에서만 | 대본 속 포스트잇 |

{: .tip }
> 오늘은 **글로벌 변수만** 사용합니다. 더 편하고, 다음 모듈(M9)에서 Flow 연결에 필요합니다.

---

## 실습 ①: FAQ Topic 만들기

| 항목 | 내용 |
|:-----|:-----|
| **Topic 이름** | FAQ Topic |
| **역할** | FAQ·복리후생·경비·휴가 문서에서 답변 찾기 → 결과 저장 |
| **글로벌 변수** | `Global.FAQ_result` |

### Step-by-Step

1. Copilot Studio → 에이전트 → 좌측 **"토픽"** 클릭
2. **"+ 토픽 추가"** → **"새로 만들기"**
3. Topic 이름 입력: `FAQ Topic`
4. **강사 제공 설정 텍스트 복붙**
5. 글로벌 변수 설정: `Global.FAQ_result`
6. **저장**

---

## 실습 ②: Contact Topic 만들기

| 항목 | 내용 |
|:-----|:-----|
| **Topic 이름** | Contact Topic |
| **역할** | 담당자정보.docx만 검색 → 담당자 반환 |
| **글로벌 변수** | `Global.Contact_result` |

동일한 방식으로 생성합니다.

---

## 실습 ③: STRICT RULES 추가

M5에서 작성한 지침에 아래 내용을 **추가**하세요:

```
## STRICT RULES
- 담당자를 찾아달라는 요청 → Contact Topic 호출
- 그 외 사내 규정/복리후생/연차/경비 질문 → FAQ Topic 호출
- Topic에서 결과를 못 찾으면 "HR팀 내선 1234로 문의해 주세요" 안내
```

{: .warning }
> STRICT RULES를 추가하지 않으면 오케스트레이터가 Topic을 **올바르게 선택**하지 못할 수 있습니다.

---

## 테스트

3가지 질문으로 Topic이 올바르게 동작하는지 확인하세요:

| # | 질문 | 기대 동작 |
|:--|:-----|:---------|
| 1 | "연차 며칠이야?" | FAQ Topic 호출 → 답변 |
| 2 | "경비처리 담당자 알려줘" | Contact Topic 호출 → 담당자 정보 |
| 3 | "아까 찾은 담당자한테 문의하고 싶어" | 포스트잇(변수) 활용 확인 |

---

## 핵심 정리

1. **Topic = 대본** — 상황별 에이전트 행동 시나리오
2. **변수 = 포스트잇** — 대화 중 정보 메모, 나중에 활용
3. **STRICT RULES** — Topic이 언제 호출되는지 명확하게 지정
4. Topic은 수집하고 처리한다. **말하는 것은 오케스트레이터**

{: .note }
> 복붙이지만 중요한 건 **"포스트잇에 뭔가를 메모하고 있구나"를 느끼는 것**입니다.

---

## FAQ

| 질문 | 답변 |
|:-----|:-----|
| Topic을 몇 개까지 만들 수 있나요? | 제한은 많지 않지만, 역할이 명확한 Topic 위주로 만드세요. |
| Topic과 지침이 충돌하면? | STRICT RULES가 우선합니다. 지침과 Topic의 역할을 명확히 구분하세요. |
| 변수 이름은 아무거나 해도 되나요? | 네. 단, `Global.` 접두사가 있으면 글로벌 변수입니다. |

---

## 참조 자료

| 자료 | 링크 |
|:-----|:-----|
| Topics 개요 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/authoring-fundamentals) |
| 변수 사용 가이드 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/authoring-variables) |
| 글로벌 변수 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/authoring-variables-bot) |

---

다음 모듈: [M8. 배포](m08-deployment)
