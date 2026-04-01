---
title: "M9. Tools — Topics and Variables"
nav_order: 10
has_children: true
---

# Tools — Topics and Variables
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 14:10 | 35 min | 🟢 Hands-on Lab |

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

![M9 Topics and Variables — Scripts and Sticky Notes](../assets/images/m09/hero.png)

---

## What You'll Learn in This Module

- Understand the **Topic = Script** analogy
- Understand the **Variable = Sticky Note** analogy
- **Build 2 Topics**: FAQ Topic + Contact Topic (copy-paste lab)
- Add **STRICT RULES** to Instructions to define when Topics are triggered

---

## Topic = Script

A Topic is a **pre-written script that defines how the agent should behave** in a specific situation.

The generative orchestrator reads the user's question and **automatically selects and runs the appropriate script**.

---

## Variable = Sticky Note

A variable is a **sticky note for jotting down information** needed during a conversation.  
It can be retrieved later by other Topics or Flows.

```
User: "Who handles expense reports?"
     ↓
Topic: "Run the find-contact script"
     ↓
📝 Sticky Note: [Contact: John Smith / Phone: 010-1234]
     ↓
User: "Submit an inquiry to the contact you just found"
     ↓
Flow: Runs using the information from the sticky note
```

### Global Variables vs Local Variables

| Type | Scope | Analogy |
|:-----|:------|:--------|
| **Global Variable** | Shared across all scripts | Sticky note pinned to your chest |
| Local Variable | Only within that script | Sticky note inside the script |

{: .tip }
> Today we'll use **global variables only**. They're easier to work with and are needed for Flow connections in later modules.

---

## Lab ①: Create the FAQ Topic

{: .important }
> 📌 This lab is on a separate page.  
> Complete [Lab ①: Create the FAQ Topic](m09-1-faq-topic) and come back here.

---

## Lab ②: Create the Contact Topic

{: .important }
> 📌 This lab is on a separate page.  
> Complete [Lab ②: Create the Contact Topic](m09-2-contact-topic) and come back here.

---

## Lab ③: Add STRICT RULES

{: .important }
> 📌 This lab is on a separate page.  
> Complete [Lab ③: Add STRICT RULES](m09-3-strict-rules) and come back here.

---

## Topic Selection Priority

When questions seem to overlap, prioritize the **more specific intent**.

| Question Type | Priority Topic | Reason |
|:--------------|:---------------|:-------|
| Contact lookup like "Who's the contact person?" | Contact Topic | The goal is to return contact information |
| Company policy inquiry like "What's the leave policy?" | FAQ Topic | The goal is to explain policies/benefits |
| Ambiguous question that could be either | Ask a follow-up | A clarifying question is safer than running the wrong Topic |

{: .note }
> In M12, when the **Request Topic** is added, messages requesting actual actions like "Submit an inquiry for me" will be prioritized to Request Topic over Contact/FAQ.

---

## Test

Verify that Topics work correctly with these 3 questions:

| # | Question | Expected Behavior |
|:--|:---------|:------------------|
| 1 | "How many vacation days do I get?" | FAQ Topic triggered → Answer |
| 2 | "Who handles expense reports?" | Contact Topic triggered → Contact info |
| 3 | "I'd like to submit an inquiry to the contact you just found" | Sticky note (variable) usage confirmed |

---

## Key Takeaways

1. **Topic = Script** — A behavior scenario for the agent per situation
2. **Variable = Sticky Note** — Notes information during conversation for later use
3. **STRICT RULES** — Clearly define when each Topic should be triggered
4. Topics collect and process. **The orchestrator does the talking**

{: .note }
> It's copy-paste, but the important thing is **feeling that "something is being noted on a sticky note."**

---

## FAQ

| Question | Answer |
|:---------|:-------|
| How many Topics can I create? | There isn't a strict limit, but focus on creating Topics with clearly defined roles. |
| What if a Topic and Instructions conflict? | STRICT RULES take priority. If multiple Topic candidates match simultaneously, prioritize the more specific request. If it's ambiguous, ask a follow-up question. |
| Can I name variables anything I want? | Yes. However, if it has the `Global.` prefix, it's a global variable. |

---

## References

| Resource | Link |
|:---------|:-----|
| Topics Overview | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/authoring-fundamentals) |
| Variable Usage Guide | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/authoring-variables) |
| Global Variables | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/authoring-variables-bot) |

---

Next module: [M10. Publish and Share](m10-publish-share)
