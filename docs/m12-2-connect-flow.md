---
title: "실습② — 에이전트에 흐름 연결"
parent: "M12. 도구 — 에이전트 흐름"
nav_order: 2
---

# 실습: 에이전트에 흐름 연결하기
{: .no_toc }

| 시간 | 소요 | 수강생 역할 |
|:-----|:-----|:-----------|
| 16:05 | 10분 | 🟢 직접 실습 |

---

## Request Topic 만들기

1. Copilot Studio → **토픽 → + 토픽 추가**
2. 이름: `Request Topic`
3. 질문 노드: 문의 내용 수집 → 변수 저장
4. 작업 노드: **RequestByEmail** 흐름 호출
5. 입력 매핑:
   - `myRequest` → 문의 내용 변수
   - `mySender` → `System.User.DisplayName`
   - `myEmail` → 담당자 메일 주소
6. 메시지 노드: 전달 완료 메시지 출력
7. **저장 → 게시**

{: .tip }
> 지침의 STRICT RULES에 "담당자 문의가 필요할 때는 반드시 Request Topic을 실행하라"고 추가하면 오케스트레이터가 이 토픽을 더 잘 채택합니다.

---

실습을 완료했으면 [M12 본문으로 돌아가세요](m12-agent-flow).
