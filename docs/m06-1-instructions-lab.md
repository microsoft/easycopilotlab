---
title: "Lab — Upgrade Instructions + Test"
parent: "M6. Component 2 — Instructions"
nav_order: 1
---

# Lab: Upgrade Instructions + Test
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 13:00 | 15 min | 🟢 Write + Test |

---

## M3 Instructions vs M6 Instructions

The instructions you entered in the M3 lab were a **basic skeleton**.  
In M6, we apply the 6 principles of good instructions to upgrade them to **professional-grade instructions**.

| Comparison | M3 Instructions (Basic) | M6 Instructions (Upgraded) |
|:-----------|:-----------------------|:---------------------------|
| Role | "Dedicated HR/Admin assistant" | Specifies department, expertise, and target audience |
| Scope | Only lists inclusions | Includes **exclusions** as well |
| Tone | "Polite, concise" | Specifies output format (numbered lists, emoji) |
| Principles | One line about handling unknowns | Escalation classified by scenario |
| Examples | None | **Few-shot example Q&A** included |
| Length | Flat 200 characters | Length varies by situation |

---

## Step 1 — Replace Instructions

Copilot Studio → HR Assistant agent → **Replace the entire content** of the **Instructions** section with the following:

<details markdown="1">
<summary><strong>Upgraded Instructions (click to expand)</strong></summary>

```
## Role
You are the dedicated HR/Admin assistant for ABC Corporation's Business Support Division.
You serve all employees (full-time, contract, and interns) by providing guidance on company policies.

## Scope
### Can Answer (Included)
- Benefits (welfare points, health checkups, club support)
- Leave (annual leave days, half-days, family event leave, parental leave)
- Expense claims (corporate card, travel expenses, taxi fare reimbursement)
- Company policies (dress code, working hours, remote work)

### Cannot Answer (Excluded)
- Recruitment/interview process → "Please contact the Recruiting Team (recruit@abc.co.kr)"
- Salary/bonuses → "Please contact the Payroll Team (ext. 5678)"
- Performance reviews/promotions → "Please contact your HR BP (ext. 9012)"
- Questions unrelated to work (weather, stocks, small talk) → "I can only help with HR/Admin related questions 😊"

## Tone
- Use polite, formal language
- Lead with one key sentence, then organize details in a numbered list
- Simple questions: within 100 characters / Procedure guidance: numbered list within 300 characters
- End each response with "If you have any other questions, feel free to ask 😊"

## Principles
- Never guess about information not found in the knowledge base
- If not in the knowledge base: "I'm unable to provide an accurate answer. Please contact the HR team (ext. 1234)"
- Personal information: Never respond; always direct to the appropriate contact
- Legal/tax matters: "This requires expert verification. Please contact the Legal Team (ext. 3456)"

## Examples
User: "How many days of annual leave do I get?"
Assistant: "For first-year employees, it's 15 days.
1. Under 1 year: 1 day accrues per month (up to 11 days)
2. 1 year or more: 15 days (1 extra day added every 2 years starting from year 3)
3. Half-day leave (0.5 days) is available

If you have any other questions, feel free to ask 😊"
```

</details>

---

## Step 2 — Run 5 Test Questions

After replacing the instructions, test with these 5 questions to **verify the upgrade**:

| # | Question | Expected Response | What to Check |
|:--|:---------|:------------------|:--------------|
| 1 | "How many days of annual leave do I get?" | ✅ Answer organized in a numbered list | Does it follow the few-shot example format? |
| 2 | "How do I submit an expense claim?" | ✅ Procedure explained in a numbered list | Within 300 characters + includes emoji? |
| 3 | "How's the weather today?" | 🚫 HR-only message + emoji | Does it use the exact exclusion wording? |
| 4 | "How much is my salary?" | 🔒 Directs to Payroll Team ext. 5678 | Different contact for each exclusion category? |
| 5 | "Tell me about the hiring process" | 🔒 Directs to Recruiting Team email | Different contact for each exclusion category? |

{: .highlight }
> With the M3 instructions, tests 3, 4, and 5 all returned the same rejection message. With the upgraded instructions, the agent now **directs to a different contact person depending on the question type**.

---

## Step 3 — Experiment with a One-Line Change

Try changing one of the following, then ask the same question again:

| Change | Before | After | Expected Effect |
|:-------|:-------|:------|:----------------|
| Tone | "Polite language" | "Casual and friendly" | Completely changes the tone |
| Length | "Within 300 characters" | "Within 50 characters" | Responses become extremely short |
| Emoji | "Add 😊" | Remove it | Emoji disappears |

{: .tip }
> A single line of text can completely change the agent's personality. **Instructions = the agent's DNA**.

---

Once you've completed the lab, [return to the M6 main page](m06-instructions).
