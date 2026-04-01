---
title: "Lab ① — Create the FAQ Topic"
parent: "M9. Tools — Topics and Variables"
nav_order: 1
---

# Lab ①: Create the FAQ Topic
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 14:10 | 10 min | 🟢 Hands-on Lab |

---

| Item | Details |
|:-----|:--------|
| **Topic Name** | FAQ Topic |
| **Role** | Find answers from FAQ, benefits, expense, and leave documents → Save results |
| **Global Variable** | `Global.FAQ_result` |

## Step-by-Step

1. Copilot Studio → Agent → Click **"Topics"** on the left
2. **"+ Add a topic"** → **"Create new"**
3. Enter Topic name: `FAQ Topic`
4. When the editing screen opens, configure the nodes in this order:

### Node 1 — Trigger (auto-generated)
- A "When the topic is triggered" node is automatically created.
- Enter the **Description**: `A script that answers FAQ questions about company policies, benefits, annual leave, expense processing, etc.`

### Node 2 — Knowledge Search (Generative Answers)
- Click **"+"** below the trigger → Add a **"Knowledge search"** node
- Search target: **All knowledge sources** (default)
- Input: `Activity.Text` (user's question)
- Output variable: **Select variable → "Create new variable"**
  - Name: `FAQ_result`
  - Check **"Set as global variable"** → It becomes `Global.FAQ_result`

### Node 3 — Message
- Click **"+"** → Add a **"Send a message"** node
- Message content: `{Global.FAQ_result}` (use the variable insert button)

5. Click **Save** on the right

{: .tip }
> The trigger's **Description** is the key. The orchestrator reads this description to decide "whether or not to use the FAQ Topic."

---

Once you've completed this lab, [return to the M9 main page](m09-topic-variables).
