---
title: "Lab ② — Connect the Flow to Your Agent"
parent: "M12. Tools — Agent Flow"
nav_order: 2
---

# Lab: Connect the Flow to Your Agent
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 16:05 | 10 min | 🟢 Hands-on Lab |

---

## Create the Request Topic

1. Copilot Studio → **Topics → + Add a topic**
2. Name: `Request Topic`
3. Question node: Collect the inquiry content → Save to a variable
4. Action node: Invoke the **RequestByEmail** flow
5. Input mapping:
   - `myRequest` → Inquiry content variable
   - `mySender` → `System.User.DisplayName`
   - `myEmail` → Contact person's email address
6. Message node: Display a confirmation message
7. **Save → Publish**

{: .tip }
> Adding a rule like "When a contact inquiry is needed, always run Request Topic" to the STRICT RULES in your instructions helps the orchestrator select this topic more reliably.

---

Once you have completed this lab, [return to the M12 main page](m12-agent-flow).
