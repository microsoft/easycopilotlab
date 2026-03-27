---
title: "M1. 코파일럿 동작원리"
nav_order: 2
---

# 코파일럿과 에이전트의 동작원리 — 당신은 AI와 대화하고 있지 않다
{: .no_toc }

| 시간 | 소요 | 수강생 역할 |
|:-----|:-----|:-----------|
| 09:40 | 10분 | 👀 보기 |

## 목차
{: .no_toc .text-delta }

1. TOC
{:toc}

![M1 동작원리 — 당신은 AI와 대화하고 있지 않다](../assets/images/m01/hero.png)

---

## 이 모듈에서 배우는 것

- 우리가 AI와 직접 대화한다는 것은 **착각**이라는 사실
- 인간과 LLM 사이에서 대화를 **중개하는 오케스트레이터**가 진짜 핵심이라는 점
- 오케스트레이터가 **시스템 프롬프트**와 **도구**를 통해 AI의 행동을 결정하는 원리
- Copilot의 오케스트레이터가 답변을 위해 **동원하는 수단들**

---

## 당신은 AI와 대화하고 있지 않다

ChatGPT에 질문을 입력하면, AI에게 직접 말하는 것 같습니다.  
하지만 **아닙니다.**

여러분과 LLM(대형 언어 모델) 사이에는 보이지 않는 **중개자**가 있습니다.  
이 중개자가 **오케스트레이터**입니다.

{: .warning }
> 우리가 사용하는 거의 모든 AI 챗봇 — ChatGPT, Copilot, Gemini, Claude — 에는 오케스트레이터가 있습니다. AI가 혼자 대답하는 서비스는 사실상 없습니다.

---

## 오케스트레이터가 하는 일

오케스트레이터는 단순한 중계기가 아닙니다.  
**판단하고, 수집하고, 가공하고, 행동하는 주체**입니다.

```mermaid
flowchart TB
    U["👤 사용자"] --> O["🚦 오케스트레이터"]
    
    O --> SP["📋 시스템 프롬프트 적용\n목적 · 태도 · 제한사항"]
    SP --> J{"어떤 수단이 필요한가?"}
    
    J --> T1["📎 첨부파일 읽기"]
    J --> T2["🔍 Bing 웹 검색"]
    J --> T3["🎨 이미지 생성"]
    J --> T4["🐍 Python 코드 실행"]
    J --> T5["📧 메일 · 📁 파일 · 📅 일정"]
    J --> T6["💬 이전 대화 기록 참조"]
    
    T1 & T2 & T3 & T4 & T5 & T6 --> LLM["🧠 LLM"]
    LLM --> A["💬 답변"]

    style O fill:#1a3a5c,color:#fff,stroke:#2563eb,stroke-width:3px
    style SP fill:#2563eb,color:#fff,stroke:#1a3a5c
    style J fill:#e8eef6,color:#1a3a5c,stroke:#2563eb,stroke-width:2px
    style LLM fill:#f7f9fc,color:#1a3a5c,stroke:#cbd5e0,stroke-width:2px
    style U fill:#fff,color:#1a3a5c,stroke:#cbd5e0
    style A fill:#fff,color:#1a3a5c,stroke:#cbd5e0
    style T1 fill:#e8eef6,color:#2c3e50,stroke:#2563eb
    style T2 fill:#e8eef6,color:#2c3e50,stroke:#2563eb
    style T3 fill:#e8eef6,color:#2c3e50,stroke:#2563eb
    style T4 fill:#e8eef6,color:#2c3e50,stroke:#2563eb
    style T5 fill:#e8eef6,color:#2c3e50,stroke:#2563eb
    style T6 fill:#e8eef6,color:#2c3e50,stroke:#2563eb
```

<div style="display:flex; justify-content:center; margin:1.5rem 0;">
<table style="border:none; border-collapse:collapse; text-align:center; background:transparent;">
<tr style="border:none;">
  <td colspan="6" style="border:none; padding:0 0 4px 0;">
    <div style="display:inline-block; background:#fff; border:2px solid #cbd5e0; border-radius:50%; width:64px; height:64px; line-height:64px; font-size:28px;">👤</div><br/>
    <small style="color:#4a5568;">사용자 질문</small>
  </td>
</tr>
<tr style="border:none;"><td colspan="6" style="border:none; padding:2px 0; color:#2563eb; font-size:22px;">⬇</td></tr>
<tr style="border:none;">
  <td colspan="6" style="border:none; padding:0;">
    <div style="background:linear-gradient(135deg,#1a3a5c,#2563eb); color:#fff; border-radius:12px; padding:14px 24px; display:inline-block; font-size:15px; font-weight:bold; letter-spacing:0.5px;">
      🚦 오케스트레이터
    </div>
  </td>
</tr>
<tr style="border:none;">
  <td colspan="6" style="border:none; padding:4px 0 2px 0;">
    <div style="background:#edf2f7; border:1px solid #cbd5e0; border-radius:8px; padding:8px 18px; display:inline-block; font-size:13px; color:#1a3a5c;">
      📋 <b>시스템 프롬프트</b> — 목적 · 태도 · 제한사항
    </div>
  </td>
</tr>
<tr style="border:none;">
  <td colspan="6" style="border:none; padding:2px 0 6px 0;">
    <span style="display:inline-block; background:#e8eef6; border:1px dashed #2563eb; border-radius:8px; padding:6px 14px; font-size:12px; color:#2563eb; font-weight:bold;">
      ❓ 어떤 수단이 필요한가?
    </span>
  </td>
</tr>
<tr style="border:none;">
  <td style="border:none; padding:3px 6px;"><div style="background:#e8eef6; border:1px solid #2563eb; border-radius:8px; padding:8px 10px; font-size:12px; color:#2c3e50; min-width:80px;">📎<br/>첨부파일<br/>읽기</div></td>
  <td style="border:none; padding:3px 6px;"><div style="background:#e8eef6; border:1px solid #2563eb; border-radius:8px; padding:8px 10px; font-size:12px; color:#2c3e50; min-width:80px;">🔍<br/>Bing<br/>웹 검색</div></td>
  <td style="border:none; padding:3px 6px;"><div style="background:#e8eef6; border:1px solid #2563eb; border-radius:8px; padding:8px 10px; font-size:12px; color:#2c3e50; min-width:80px;">🎨<br/>이미지<br/>생성</div></td>
  <td style="border:none; padding:3px 6px;"><div style="background:#e8eef6; border:1px solid #2563eb; border-radius:8px; padding:8px 10px; font-size:12px; color:#2c3e50; min-width:80px;">🐍<br/>Python<br/>코드 실행</div></td>
  <td style="border:none; padding:3px 6px;"><div style="background:#e8eef6; border:1px solid #2563eb; border-radius:8px; padding:8px 10px; font-size:12px; color:#2c3e50; min-width:80px;">📧<br/>메일·파일<br/>일정</div></td>
  <td style="border:none; padding:3px 6px;"><div style="background:#e8eef6; border:1px solid #2563eb; border-radius:8px; padding:8px 10px; font-size:12px; color:#2c3e50; min-width:80px;">💬<br/>대화 기록<br/>참조</div></td>
</tr>
<tr style="border:none;"><td colspan="6" style="border:none; padding:2px 0; color:#2563eb; font-size:22px;">⬇</td></tr>
<tr style="border:none;">
  <td colspan="6" style="border:none; padding:0 0 4px 0;">
    <div style="display:inline-block; background:#f7f9fc; border:2px solid #cbd5e0; border-radius:10px; padding:8px 20px; font-size:14px; color:#1a3a5c;">🧠 <b>LLM</b></div>
  </td>
</tr>
<tr style="border:none;"><td colspan="6" style="border:none; padding:2px 0; color:#2563eb; font-size:22px;">⬇</td></tr>
<tr style="border:none;">
  <td colspan="6" style="border:none; padding:0;">
    <div style="display:inline-block; background:#fff; border:2px solid #cbd5e0; border-radius:10px; padding:8px 20px; font-size:14px; color:#1a3a5c;">💬 <b>답변</b></div>
  </td>
</tr>
</table>
</div>

오케스트레이터가 하는 일을 세 가지로 정리하면:

### 1. 성격을 부여한다 — 시스템 프롬프트

오케스트레이터는 LLM에게 질문을 넘기기 **전에**, 시스템 프롬프트를 먼저 설정합니다.

> "너는 Microsoft 365 Copilot이다. 사용자의 업무를 돕는 것이 목적이다. 정치적 의견은 말하지 마라. 답변은 한국어로 하라."

이 시스템 프롬프트가 AI의 **목적, 태도, 제약**을 결정합니다.  
같은 GPT-4o 모델이라도, 시스템 프롬프트가 다르면 전혀 다른 AI처럼 동작합니다.

| 서비스 | 같은 LLM | 시스템 프롬프트 | 결과 |
|:-------|:---------|:------------|:-----|
| ChatGPT | GPT-4o | "범용 AI 어시스턴트" | 무엇이든 대답하는 만능 비서 |
| Copilot | GPT-4o | "M365 업무 도우미, 회사 데이터 참조" | 내 이메일·파일을 아는 업무 도우미 |
| **우리가 만들 에이전트** | GPT-4o | **"HR 전문 도우미, 사내 규정 참조"** | **HR 질문만 답하는 전문가** |

{: .highlight }
> 오늘 오후 실습에서 여러분이 작성할 **지침(Instructions)**이 바로 이 시스템 프롬프트입니다.

### 2. 수단을 동원한다 — 도구 호출

오케스트레이터는 질문에 답하기 위해 **할 수 있는 모든 수단을 동원**합니다.

| 상황 | 오케스트레이터가 하는 일 |
|:-----|:---------------------|
| 사용자가 파일을 첨부했다 | 📎 파일 내용을 읽어서 LLM에 전달 |
| "오늘 환율 알려줘" | 🔍 Bing 검색으로 최신 환율을 가져온 뒤 LLM에 전달 |
| "이 데이터로 그래프 그려줘" | 🐍 Python 코드를 작성·실행하여 차트 생성 |
| "이 내용을 그림으로 만들어줘" | 🎨 DALL-E로 이미지를 생성 |
| "지난주 팀 회의 내용 정리해줘" | 📧 Teams 대화 기록을 검색하여 LLM에 전달 |
| 이전 대화에서 선호도를 말했다 | 💬 대화 기록에서 사용자 선호를 추출하여 반영 |

이 중 어느 것도 LLM이 스스로 하는 일이 아닙니다.  
**모두 오케스트레이터가 판단하고 실행하는 일**입니다.

{: .tip }
> LLM은 텍스트를 생성하는 엔진일 뿐입니다. 인터넷을 검색하거나, 파일을 읽거나, 코드를 실행하는 것은 **오케스트레이터의 판단 아래 도구가 수행하는 것**입니다.

### 3. 맥락을 관리한다 — 대화 기록과 사용자 정보

오케스트레이터는 한 번의 질문만 보는 것이 아닙니다.

- **이전 대화 기록**을 기억하여 "아까 그 파일"이라고 하면 무슨 파일인지 파악
- 사용자가 선호하는 **언어, 호칭, 답변 스타일**을 대화에서 추출하여 반영
- 필요하면 **사용자에게 되물어서** 모호한 질문을 명확히 함

---

## 같은 LLM, 다른 오케스트레이터, 다른 결과

이 원리를 이해하면, ChatGPT와 Copilot이 왜 다른지 명확해집니다.

```mermaid
flowchart TB
    subgraph A ["ChatGPT"]
        direction TB
        Q1["👤 질문"] --> O1["🚦 범용 오케스트레이터\n웹검색 · 코드실행"]
    end
    
    subgraph B ["Copilot"]
        direction TB
        Q2["👤 질문"] --> O2["🚦 M365 오케스트레이터\n업무특화 · M365데이터"]
    end
    
    subgraph C ["우리 에이전트"]
        direction TB
        Q3["👤 질문"] --> O3["🚦 우리가 만든 오케스트레이터\nHR특화 · 사내규정 · 커넥터"]
    end
    
    O1 & O2 & O3 --> LLM["🧠 같은 GPT-4o"]

    style O1 fill:#6b7280,color:#fff,stroke:#4b5563,stroke-width:2px
    style O2 fill:#2563eb,color:#fff,stroke:#1a3a5c,stroke-width:2px
    style O3 fill:#1a3a5c,color:#fff,stroke:#2563eb,stroke-width:3px
    style LLM fill:#f7f9fc,color:#1a3a5c,stroke:#cbd5e0,stroke-width:2px
```

<div style="display:flex; justify-content:center; margin:1.5rem 0;">
<table style="border:none; border-collapse:collapse; text-align:center; background:transparent; max-width:720px;">
<tr style="border:none;">
  <td style="border:none; padding:6px 10px; vertical-align:top; width:33%;">
    <div style="border:2px solid #cbd5e0; border-radius:12px; padding:14px 10px; background:#fff;">
      <div style="font-size:13px; color:#6b7280; font-weight:bold; margin-bottom:8px;">ChatGPT</div>
      <div style="background:#6b7280; color:#fff; border-radius:8px; padding:10px 8px; font-size:12px; line-height:1.6;">
        🚦 <b>범용 오케스트레이터</b><br/>
        <span style="font-size:11px;">웹검색 · 코드실행 · 이미지생성</span>
      </div>
      <div style="margin-top:8px; font-size:11px; color:#6b7280; line-height:1.5;">
        📋 "범용 AI 어시스턴트"<br/>
        🗂 사용자가 직접 제공
      </div>
    </div>
  </td>
  <td style="border:none; padding:6px 10px; vertical-align:top; width:33%;">
    <div style="border:2px solid #2563eb; border-radius:12px; padding:14px 10px; background:#fff;">
      <div style="font-size:13px; color:#2563eb; font-weight:bold; margin-bottom:8px;">Copilot</div>
      <div style="background:#2563eb; color:#fff; border-radius:8px; padding:10px 8px; font-size:12px; line-height:1.6;">
        🚦 <b>M365 오케스트레이터</b><br/>
        <span style="font-size:11px;">업무특화 · M365데이터 · 웹검색</span>
      </div>
      <div style="margin-top:8px; font-size:11px; color:#2563eb; line-height:1.5;">
        📋 "M365 업무 도우미"<br/>
        🗂 이메일 · 파일 · 일정 · Teams
      </div>
    </div>
  </td>
  <td style="border:none; padding:6px 10px; vertical-align:top; width:33%;">
    <div style="border:3px solid #1a3a5c; border-radius:12px; padding:14px 10px; background:#f7f9fc; box-shadow:0 2px 8px rgba(26,58,92,0.15);">
      <div style="font-size:13px; color:#1a3a5c; font-weight:bold; margin-bottom:8px;">⭐ 우리 에이전트</div>
      <div style="background:linear-gradient(135deg,#1a3a5c,#2563eb); color:#fff; border-radius:8px; padding:10px 8px; font-size:12px; line-height:1.6;">
        🚦 <b>우리가 만든 오케스트레이터</b><br/>
        <span style="font-size:11px;">HR특화 · 사내규정 · 커넥터 · 흐름</span>
      </div>
      <div style="margin-top:8px; font-size:11px; color:#1a3a5c; line-height:1.5;">
        📋 "HR 전문 도우미"<br/>
        🗂 사내규정 · Excel · 커넥터
      </div>
    </div>
  </td>
</tr>
<tr style="border:none;">
  <td colspan="3" style="border:none; padding:4px 0; color:#2563eb; font-size:18px;">⬇&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⬇&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⬇</td>
</tr>
<tr style="border:none;">
  <td colspan="3" style="border:none; padding:0;">
    <div style="display:inline-block; background:#f7f9fc; border:2px solid #cbd5e0; border-radius:10px; padding:10px 40px; font-size:14px; color:#1a3a5c;">
      🧠 <b>같은 GPT-4o 엔진</b>
    </div>
  </td>
</tr>
<tr style="border:none;">
  <td colspan="3" style="border:none; padding:6px 0 0 0;">
    <span style="font-size:12px; color:#4a5568;">LLM은 같다. <b style="color:#1a3a5c;">오케스트레이터가 다르면 결과가 다르다.</b></span>
  </td>
</tr>
</table>
</div>

세 서비스 모두 **같은 GPT-4o**를 사용할 수 있습니다.  
하지만 결과가 다른 이유는 **오케스트레이터가 다르기 때문**입니다.

| 비교 | ChatGPT | Copilot | 우리가 만들 에이전트 |
|:-----|:--------|:--------|:-----------------|
| **시스템 프롬프트** | 범용 어시스턴트 | M365 업무 도우미 | HR 전문 도우미 |
| **접근 가능한 데이터** | 없음 (사용자가 직접 제공) | 이메일, 파일, 일정, Teams | 사내 규정 문서, Excel, 커넥터 |
| **사용 가능한 도구** | 웹검색, 코드실행, 이미지생성 | + M365 Graph API | + 토픽, 커넥터, 에이전트 흐름 |
| **결과** | 일반적인 답변 | 내 업무 맥락이 반영된 답변 | **우리 회사 HR 규정에 맞는 답변** |

---

## 오늘 우리가 하는 일의 본질

오늘 하루 동안 우리가 하는 것은 결국 이것입니다:

> **우리만의 오케스트레이터를 설계하는 것**

| 오케스트레이터 구성요소 | 오늘 실습에서 하는 일 | 모듈 |
|:---------------------|:-------------------|:-----|
| 시스템 프롬프트 (성격) | **지침** 작성 | M6 |
| 참조 데이터 (지식) | **지식 소스** 연결 | M7 |
| 도구 (행동 수단) | **토픽, 커넥터, 흐름** 연결 | M8~M16 |
| 판단 엔진 (두뇌) | **오케스트레이터 설정** | M5 |

---

## 핵심 정리

1. 우리는 AI와 직접 대화하지 않는다 — **오케스트레이터가 중개**한다
2. 오케스트레이터가 **시스템 프롬프트**로 AI의 성격과 제약을 결정한다
3. 오케스트레이터가 **모든 수단을 동원**하여 답변을 만든다 — 파일 읽기, 웹 검색, 코드 실행, 이미지 생성 모두 오케스트레이터의 판단
4. 같은 LLM이라도 **오케스트레이터가 다르면 전혀 다른 결과**가 나온다
5. 오늘 우리가 하는 일은 **우리만의 오케스트레이터를 설계하는 것**이다

---

## FAQ

| 질문 | 답변 |
|:-----|:-----|
| ChatGPT와 Copilot의 가장 큰 차이는? | LLM이 아니라 **오케스트레이터**가 다릅니다. Copilot은 M365 데이터에 접근하는 오케스트레이터를 가지고 있습니다. |
| AI가 거짓말(할루시네이션)을 하면? | LLM은 본질적으로 "그럴듯한 다음 단어"를 생성합니다. 이를 줄이는 것이 오케스트레이터의 역할이며, **지식 소스 연결**과 **지침 설정**이 핵심 수단입니다. |
| 왜 에이전트를 따로 만들어야 하나요? | Copilot은 범용 오케스트레이터입니다. 우리 회사 HR 규정을 모릅니다. **특화된 오케스트레이터**를 만들어야 정확한 답변이 나옵니다. |

---

## 참조 자료

| 자료 | 링크 |
|:-----|:-----|
| Microsoft Copilot 공식 문서 | [learn.microsoft.com/copilot](https://learn.microsoft.com/copilot/) |
| Copilot Studio 시작하기 | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/fundamentals-get-started) |

---

다음 모듈: [M2. 몰입형 vs 인컨텍스트](m02-immersive-incontext)
