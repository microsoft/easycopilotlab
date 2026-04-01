---
title: "Lab ② — Create the Contact Topic"
parent: "M9. Tools — Topics and Variables"
nav_order: 2
---

# Lab ②: Create the Contact Topic
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 14:20 | 10 min | 🟢 Hands-on Lab |

---

| Item | Details |
|:-----|:--------|
| **Topic Name** | Contact Topic |
| **Role** | Search only 담당자정보.docx → Return contact person |
| **Global Variable** | `Global.Contact_result` |

## Step-by-Step

Create it the same way as the FAQ Topic, but with these differences:

1. Topic name: `Contact Topic`
2. Trigger Description: `A script that looks up contact names, phone numbers, and email addresses`
3. Knowledge search node: Set the search target to **"담당자정보.docx" only** (specify a particular knowledge source)
4. Output variable: `Global.Contact_result` (set as global variable)
5. Message node: `{Global.Contact_result}`
6. **Save**

---

Once you've completed this lab, [return to the M9 main page](m09-topic-variables).
