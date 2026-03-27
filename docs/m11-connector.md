---
title: "M11. 도구 — 커넥터"
nav_order: 12
has_children: true
---

# 도구 — 커넥터
{: .no_toc }

| 시간 | 소요 | 수강생 역할 |
|:-----|:-----|:-----------|
| 15:20 | 30분 | 🟢 직접 실습 |

## 목차
{: .no_toc .text-delta }

1. TOC
{:toc}

![M11 커넥터 — 자동으로 일기 쓰는 AI](../assets/images/m11/hero.png)

---

## 이 모듈에서 배우는 것

- **커넥터(Connector)**란 무엇인지 — Microsoft 365 앱을 에이전트에 직접 연결하는 원리
- 커넥터와 에이전트 흐름의 **차이점**
- Excel **행 추가 커넥터**를 활용한 **대화기록 자동 저장** 실습
- Record Topic에서 **Excel 커넥터를 직접 호출**해 대화가 Excel에 자동으로 쌓이는 것 확인

---

## 커넥터란?

**커넥터**는 Microsoft 365 앱(예: Excel, Outlook, Teams, SharePoint)에 에이전트를 하나의 동작으로 **직접 연결**하는 가장 간단한 도구입니다.

| 커넥터 | 에이전트 흐름(M12) |
|:--------|:----------------|
| 단일 앱 직접 연결 | 여러 단계 자동화 |
| 단순한 동작 | 복잡한 로직 담당 |
| 빠른 적용 | 높은 유연성 |

{: .highlight }
> 커넥터는 M365 앱 범위 내에서 단순한 작업에 적합하고, 에이전트 흐름은 **여러 단계를 엮어 복잡한 자동화**에 적합합니다.

이 모듈에서는 Excel **행 추가 커넥터**를 예시로 사용합니다. Topic 안에서 커넥터를 바로 호출해, 에이전트와 대화한 내용이 Excel에 자동으로 기록되게 만듭니다.

---

## 왜 대화를 정리합니까?

에이전트의 모든 대화를 **자동으로 Excel에 기록**하면 3가지 가치가 생깁니다.

| 목적 | 설명 |
|:-----|:-----|
| **에이전트 개선** | 자주 묻는 질문 파악 → 지식 보강 |
| **감사/컴플라이언스** | 누가, 언제, 뭘 물어봤는지 투명한 기록 |
| **업무 분석** | 질문 패턴으로 실제 업무 니즈 발견 |

---

## 대화기록 구조

```mermaid
flowchart LR
    A[👤 질문] --> B[🤖 에이전트 답변]
    B --> C[🎬 Record Topic<br>자동 트리거]
   C --> D[🔌 Excel 행 추가<br>커넥터 호출]
   D --> E[📊 Excel에<br>행 자동 추가]
```

### Excel 기록 항목

| 컬럼 | 값 | 설명 |
|:-----|:---|:-----|
| 시간 | `utcNow()` | 대화 발생 시각 |
| 사용자 | `System.User.PrincipalName` | 질문한 사람 |
| 질문 | `System.Activity.Text` | 사용자 입력 |
| 답변 | `System.Response.FormattedText` | 에이전트 응답 |

### Record Topic의 특별한 점

일반 Topic은 사용자가 특정 질문을 해야 실행됩니다.  
하지만 Record Topic은 **"AI가 응답을 생성할 때마다"** 자동 실행됩니다.

{: .highlight }
> 사용자는 기록되는 줄도 모릅니다. 에이전트가 **자동으로 일기를 쓰는 것**입니다.

---

## 실습 ①: Excel 파일 준비

{: .important }
> 📌 이 실습은 별도 페이지에서 진행합니다.  
> [실습 ①: Excel 파일 준비](m11-1-excel-prep)를 완료하고 돌아오세요.

---

## 실습 ②: Record Topic에서 Excel 커넥터 연결하기

{: .important }
> 📌 이 실습은 별도 페이지에서 진행합니다.  
> [실습 ②: Record Topic + Excel 커넥터](m11-2-record-topic)를 완료하고 돌아오세요.

---

## 데이터 활용 시나리오

기록된 데이터로 이런 분석이 가능합니다.

| 시나리오 | 분석 방법 | 기대 효과 |
|:---------|:---------|:---------|
| **자주 묻는 질문 TOP 10** | 질문 컬럼 키워드 분류 | 지식 소스 보강 우선순위 |
| **답변 실패 패턴** | "모르겠습니다" 필터링 | 부족한 교과서 파악 |
| **사용량 추이** | 시간대별/요일별 집계 | 서비스 시간 최적화 |
| **사용자별 현황** | Pivot 분석 | 교육 대상 파악 |

{: .tip }
> Copilot에게 "이 데이터에서 가장 많이 묻는 질문 TOP 5를 알려줘"라고 물으면 **자동으로 분석**해 줍니다.

---

## M12로 넘어가기

강사는 아래처럼 연결하면 자연스럽습니다.

> 방금 한 것은 Power Automate 흐름을 만든 것이 아니라, **Topic 안에서 Excel 커넥터를 바로 호출해 한 줄을 저장한 것**입니다. 즉, 앱 하나에 단일 동작을 바로 붙여본 것입니다. 다음 M12에서는 여기서 한 단계 더 나아가, 정보를 수집하고 AI로 문안을 만들고 메일까지 보내는 **여러 단계 자동화 흐름**으로 확장하겠습니다.

---

## 핵심 정리

1. **Record Topic** = 모든 대화를 자동으로 감지하는 특수 Topic
2. **Excel 행 추가 커넥터** = Topic 안에서 바로 호출해 대화 내용을 자동 기록
3. 기록된 데이터로 **에이전트 개선·감사·업무 분석** 가능
4. M12에서는 이 단일 동작을 넘어, **여러 단계를 묶는 Agent Flow**로 확장합니다

---

## FAQ

| 질문 | 답변 |
|:-----|:-----|
| Excel 말고 다른 곳에 저장할 수 있나요? | Dataverse, SQL, SharePoint 리스트 등 가능합니다. Excel이 가장 간단합니다. |
| Excel에 행 제한이 있나요? | 있습니다. 대량 운영 시 Dataverse나 DB를 권장합니다. |
| 개인정보 보호는 어떻게 하나요? | M1의 보안 정책이 적용됩니다. 사용자명 익명화도 가능합니다. |
| OneDrive가 막혀 있으면 어떻게 하나요? | SharePoint 문서 라이브러리나 Dataverse 같은 대체 저장소로 같은 구조를 구현할 수 있습니다. |
| 바로 오늘 팀에서 쓸 수 있나요? | 커넥터 연결과 저장소 권한이 모두 준비돼 있으면 바로 사용 가능합니다. |

---

## 참조 자료

| 자료 | 링크 |
|:-----|:-----|
| Copilot Studio 분석 대시보드 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/analytics-overview) |
| Power Automate Excel 커넥터 | [learn.microsoft.com](https://learn.microsoft.com/connectors/excelonlinebusiness/) |
| 에이전트 성능 모니터링 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/analytics-sessions) |

---

다음 모듈: [M12. 도구 — 에이전트 흐름](m12-agent-flow)
