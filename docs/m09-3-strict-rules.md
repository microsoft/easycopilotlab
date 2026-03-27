---
title: "실습③ — STRICT RULES 추가"
parent: "M9. 도구 — 토픽과 변수"
nav_order: 3
---

# 실습 ③: STRICT RULES 추가
{: .no_toc }

| 시간 | 소요 | 수강생 역할 |
|:-----|:-----|:-----------|
| 14:30 | 10분 | 🟢 직접 실습 |

---

M6에서 작성한 지침에 아래 내용을 **추가**하세요:

<details markdown="1">
<summary><strong>STRICT RULES (클릭해서 펼치기)</strong></summary>

```
## STRICT RULES
- 담당자를 찾아달라는 요청 → Contact Topic 호출
- 그 외 사내 규정/복리후생/연차/경비 질문 → FAQ Topic 호출
- Topic에서 결과를 못 찾으면 "HR팀 내선 1234로 문의해 주세요" 안내
```

</details>

{: .warning }
> STRICT RULES를 추가하지 않으면 오케스트레이터가 Topic을 **올바르게 선택**하지 못할 수 있습니다.

## 테스트

3가지 질문으로 Topic이 올바르게 동작하는지 확인하세요:

| # | 질문 | 기대 동작 |
|:--|:-----|:---------|
| 1 | "연차 며칠이야?" | FAQ Topic 호출 → 답변 |
| 2 | "경비처리 담당자 알려줘" | Contact Topic 호출 → 담당자 정보 |
| 3 | "아까 찾은 담당자한테 문의하고 싶어" | 포스트잇(변수) 활용 확인 |

---

실습을 완료했으면 [M9 본문으로 돌아가세요](m09-topic-variables).
