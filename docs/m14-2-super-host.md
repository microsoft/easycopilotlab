---
title: "Lab ② — Create the Super Host"
parent: "M14. Tools — Multi-Agent"
nav_order: 2
---

# Lab: Create the Super Host Agent
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 16:55 | 10 min | 🟢 Hands-on Lab |

---

1. Copilot Studio → **+ New agent**
2. Name: `Super Host`
3. **Actions → + Add action → Connect an agent**
4. Connect **HR Assistant** → Enter Description: "Questions about HR, benefits, leave, and expenses"
5. Connect **Legal Agent** → Enter Description: "Questions about contracts, policies, and compliance"
6. Write instructions:
   - "Delegate HR-related questions to the HR Assistant, and legal-related questions to the Legal Agent"
7. **Save → Publish**
8. Test: Enter a mix of HR and legal questions and verify which agent handles each one

## Sample Test Questions

| # | Question | Expected Routing |
|:--|:---------|:-----------------|
| 1 | "How many leave days do I have?" | → HR Assistant |
| 2 | "What's the probation period policy in the employment contract?" | → Legal Agent |
| 3 | "Where can I use my welfare points?" | → HR Assistant |
| 4 | "What's the consent withdrawal process under the data protection law?" | → Legal Agent |

{: .tip }
> The **clearer each agent's Description**, the better the Super Host selects the right agent. Write your Descriptions as specifically as possible.

---

Once you have completed this lab, [return to the M14 main page](m14-multi-agent).
