---
title: "Lab ① — Create a Legal Agent"
parent: "M14. Tools — Multi-Agent"
nav_order: 1
---

# Lab: Create a Legal Agent
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 16:45 | 10 min | 🟢 Hands-on Lab |

---

## Step 1 — Create the Agent

1. Copilot Studio → **+ New agent**
2. Name: `Legal Agent`

## Step 2 — Enter Instructions

<details markdown="1">
<summary><strong>Instructions (click to expand)</strong></summary>

```
## Role
You are our company's dedicated legal and compliance assistant.

## Scope
Only answer questions about contracts, internal policies, legal reviews, and compliance.

## Tone
- Use polite, professional language
- Explain legal terms in plain language
- State the key conclusion first, then cite the supporting clauses afterward

## Principles
- If the answer is not in your knowledge: "This requires a formal legal review. Please contact the Legal team (ext. 5678)."
- If the question constitutes legal advice: "This falls under legal counsel. Please consult directly with a Legal team representative."
- Always include the source (law name, article number) in your response
```

</details>

## Step 3 — Connect a Knowledge Source (Website)

Give the Legal Agent a **textbook**. Connect a public legal information website as a knowledge source.

1. Click **"Knowledge"** on the left → **"+ Add knowledge"**
2. Select **"Website"**
3. Enter URL: `https://law.go.kr/`
4. Name: `National Law Information Center`
5. **Save**

{: .note }
> A website knowledge source periodically crawls the site's public content for reference. Crawling may be restricted in lab environments — if so, you can upload sample legal documents as files instead.

---

Once you have completed this lab, [return to the M14 main page](m14-multi-agent).
