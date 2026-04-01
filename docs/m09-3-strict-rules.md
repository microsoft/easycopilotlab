---
title: "Lab ③ — Add STRICT RULES"
parent: "M9. Tools — Topics and Variables"
nav_order: 3
---

# Lab ③: Add STRICT RULES
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 14:30 | 10 min | 🟢 Hands-on Lab |

---

**Add** the following to the Instructions you wrote in M6:

<details markdown="1">
<summary><strong>STRICT RULES (click to expand)</strong></summary>

```
## STRICT RULES
- Requests to find a contact person → Trigger Contact Topic
- All other questions about company policies / benefits / leave / expenses → Trigger FAQ Topic
- If a Topic cannot find a result → Respond with "Please contact the HR team at extension 1234"
```

</details>

{: .warning }
> Without STRICT RULES, the orchestrator may not **select the correct Topic**.

## Test

Verify that Topics work correctly with these 3 questions:

| # | Question | Expected Behavior |
|:--|:---------|:------------------|
| 1 | "How many vacation days do I get?" | FAQ Topic triggered → Answer |
| 2 | "Who handles expense reports?" | Contact Topic triggered → Contact info |
| 3 | "I'd like to submit an inquiry to the contact you just found" | Sticky note (variable) usage confirmed |

---

Once you've completed this lab, [return to the M9 main page](m09-topic-variables).
