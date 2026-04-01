---
title: "Lab — Connect a Forms Trigger"
parent: "M16. Tools — Triggers"
nav_order: 1
---

# Lab: Connect a Forms Trigger
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 17:25 | 20 min | 🟢 Hands-on Lab |

---

## Prerequisites

1. Create an **HR Inquiry Form** in Microsoft Forms
   - Question ①: Name
   - Question ②: Department
   - Question ③: Inquiry details
2. Copy the form URL

## Steps

1. Power Automate → **+ New flow → Automated cloud flow**
2. Trigger: Select **Forms → When a new response is submitted**
3. Form ID: Select the HR Inquiry Form you created above
4. Add the **Forms → Get response details** action
5. Add the **AI Builder → AI Prompt** action
   - Prompt: "Draft a response to the following HR inquiry: [Inquiry details]"
6. Add the **Office 365 Outlook → Send an email** action
   - To: Assignee's email address
   - Body: Original inquiry + AI-generated draft
7. **Save → Test**
   - Submit a test inquiry through Forms
   - Verify that the draft arrives in the assignee's inbox

---

Once you've completed the lab, [return to the M16 overview](m16-trigger).
