---
title: "M9. 도구 — 토픽과 변수"
nav_order: 10
has_children: true
---

# 도구 — 토픽과 변수
{: .no_toc }

| 시간 | 소요 | 수강생 역할 |
|:-----|:-----|:-----------|
| 14:10 | 35분 | 🟢 직접 실습 |

## 목차
{: .no_toc .text-delta }

1. TOC
{:toc}

![M9 토픽과 변수 — 대본과 포스트잇](../assets/images/m09/hero.png)

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
> 오늘은 **글로벌 변수만** 사용합니다. 더 편하고, 이후 모듈에서 Flow 연결에 필요합니다.

---

## 실습 ①: FAQ Topic 만들기

{: .important }
> 📌 이 실습은 별도 페이지에서 진행합니다.  
> [실습 ①: FAQ Topic 만들기](m09-1-faq-topic)를 완료하고 돌아오세요.

---

## 실습 ②: Contact Topic 만들기

{: .important }
> 📌 이 실습은 별도 페이지에서 진행합니다.  
> [실습 ②: Contact Topic 만들기](m09-2-contact-topic)를 완료하고 돌아오세요.

---

## 실습 ③: STRICT RULES 추가

{: .important }
> 📌 이 실습은 별도 페이지에서 진행합니다.  
> [실습 ③: STRICT RULES 추가](m09-3-strict-rules)를 완료하고 돌아오세요.

---

## Topic 선택 우선순위

질문이 겹쳐 보일 때는 **더 구체적인 의도**를 우선합니다.

| 질문 유형 | 우선 Topic | 이유 |
|:----------|:-----------|:-----|
| "담당자 알려줘"처럼 연락처 조회 | Contact Topic | 담당자 정보 반환이 목적 |
| "연차 규정 알려줘"처럼 사내 규정 문의 | FAQ Topic | 규정/복리후생 설명이 목적 |
| 둘 다 섞여 애매한 질문 | 재질문 | 잘못된 Topic 실행보다 확인 질문이 안전 |

{: .note }
> M12에서 **Request Topic**이 추가되면, "문의 넣어줘"처럼 실제 행동을 요청하는 문장은 Contact/FAQ보다 Request Topic을 우선하도록 확장합니다.

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
| Topic과 지침이 충돌하면? | STRICT RULES가 우선합니다. 여러 Topic 후보가 동시에 맞으면 더 구체적인 요청을 우선하고, 애매하면 재질문하세요. |
| 변수 이름은 아무거나 해도 되나요? | 네. 단, `Global.` 접두사가 있으면 글로벌 변수입니다. |

---

## 참조 자료

| 자료 | 링크 |
|:-----|:-----|
| Topics 개요 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/authoring-fundamentals) |
| 변수 사용 가이드 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/authoring-variables) |
| 글로벌 변수 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/authoring-variables-bot) |

---

다음 모듈: [M10. 게시와 공유](m10-publish-share)
