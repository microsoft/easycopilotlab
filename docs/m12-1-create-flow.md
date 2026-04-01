---
title: "Lab ① — Create a Flow"
parent: "M12. Tools — Agent Flow"
nav_order: 1
---

# Lab: Create a Power Automate Flow
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 15:50 | 15 min | 🟢 Hands-on Lab |

---

## Flow Structure — RequestByEmail

| Item | Details |
|:-----|:--------|
| **Flow name** | RequestByEmail |
| **Trigger** | When a flow is invoked from Copilot Studio |
| **Input ①** | `myRequest` (text): Inquiry content |
| **Input ②** | `mySender` (text): Sender's name |
| **Input ③** | `myEmail` (text): Contact person's email address |
| **Action ①** | Generate email body with an AI Prompt |
| **Action ②** | Send email via Office 365 Outlook |
| **Output** | `myReturn`: Completion message |

## Lab Steps

1. Go to [Power Automate](https://make.powerautomate.com)
2. Select **Create → Instant cloud flow**
3. Trigger: Select **When a flow is invoked from Copilot Studio**
4. Add 3 input variables (`myRequest`, `mySender`, `myEmail`)
5. Add an **AI Builder → AI Prompt** action → Enter the email body generation prompt
6. Add an **Office 365 Outlook → Send an email** action
7. Add the output variable `myReturn`
8. **Save → Publish**

{: .important }
> AI Builder Prompts require AI Builder credits. Depending on your organization's policies, this may not be available. If so, skip the AI Prompt step and compose the email body manually.

{: .note }
> The goal of this module is to **try adding a text-based AI Prompt once**. The different types of AI Prompts and advanced scenarios are covered separately in M13.

---

Once you have completed this lab, [return to the M12 main page](m12-agent-flow).
