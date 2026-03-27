---
title: "실습② — Contact Topic 만들기"
parent: "M9. 도구 — 토픽과 변수"
nav_order: 2
---

# 실습 ②: Contact Topic 만들기
{: .no_toc }

| 시간 | 소요 | 수강생 역할 |
|:-----|:-----|:-----------|
| 14:20 | 10분 | 🟢 직접 실습 |

---

| 항목 | 내용 |
|:-----|:-----|
| **Topic 이름** | Contact Topic |
| **역할** | 담당자정보.docx만 검색 → 담당자 반환 |
| **글로벌 변수** | `Global.Contact_result` |

## Step-by-Step

FAQ Topic과 동일한 방식으로 생성하되, 아래만 다릅니다:

1. Topic 이름: `Contact Topic`
2. 트리거 Description: `담당자 이름, 연락처, 이메일을 조회하는 대본`
3. 지식 검색 노드: 검색 대상을 **"담당자정보.docx"만 선택** (특정 지식 소스 지정)
4. 출력 변수: `Global.Contact_result` (글로벌 변수로 설정)
5. 메시지 노드: `{Global.Contact_result}`
6. **저장**

---

실습을 완료했으면 [M9 본문으로 돌아가세요](m09-topic-variables).
