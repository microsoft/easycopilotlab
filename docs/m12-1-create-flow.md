---
title: "실습① — 흐름 만들기"
parent: "M12. 도구 — 에이전트 흐름"
nav_order: 1
---

# 실습: Power Automate 흐름 만들기
{: .no_toc }

| 시간 | 소요 | 수강생 역할 |
|:-----|:-----|:-----------|
| 15:50 | 15분 | 🟢 직접 실습 |

---

## 흐름 구조 — RequestByEmail

| 항목 | 내용 |
|:-----|:-----|
| **흐름 이름** | RequestByEmail |
| **트리거** | Copilot Studio에서 흐름을 호출할 때 |
| **입력 ①** | `myRequest` (텍스트): 문의 내용 |
| **입력 ②** | `mySender` (텍스트): 문의자 이름 |
| **입력 ③** | `myEmail` (텍스트): 담당자 메일 주소 |
| **동작 ①** | AI 프롬프트로 메일 본문 생성 |
| **동작 ②** | Office 365 Outlook으로 메일 발송 |
| **출력** | `myReturn`: 완료 메시지 |

## 실습 순서

1. [Power Automate](https://make.powerautomate.com) 접속
2. **만들기 → 즉시 클라우드 흐름** 선택
3. 트리거: **Copilot Studio에서 흐름을 호출할 때** 선택
4. 입력 변수 3개 추가 (`myRequest`, `mySender`, `myEmail`)
5. **AI Builder → AI 프롬프트** 동작 추가 → 메일 본문 생성 프롬프트 입력
6. **Office 365 Outlook → 메일 보내기** 동작 추가
7. 출력 변수 `myReturn` 추가
8. **저장 → 게시**

{: .important }
> AI Builder 프롬프트는 AI Builder 크레딧이 필요합니다. 조직 정책에 따라 사용 불가일 수 있습니다. 이 경우 AI 프롬프트 단계를 건너뛰고 직접 메일 본문을 작성합니다.

{: .note }
> 이 모듈의 목표는 **텍스트 AI 프롬프트를 한 번 넣어 보는 것**입니다. AI 프롬프트의 종류와 확장 시나리오는 다음 M13에서 따로 정리합니다.

---

실습을 완료했으면 [M12 본문으로 돌아가세요](m12-agent-flow).
