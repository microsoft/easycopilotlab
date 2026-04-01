---
title: "M7. Element 3 — Knowledge"
nav_order: 8
has_children: true
---

# Element 3 — Knowledge: RAG Concepts + Reference Document Upload
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 13:30 | 30 min | 🟢 Hands-on Lab |

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

![M7 Knowledge — Uploading the Textbook](../assets/images/m07/hero.png)

---

## What You'll Learn in This Module

- Connect a knowledge source by **uploading files directly** to Copilot Studio
- Experience the **before-and-after difference** in answer quality after adding a knowledge source
- Understand the differences between 4 ways to connect knowledge
- How **document structure** affects answer quality

---

## The More It Knows, the Better It Answers

In M6, we wrote Instructions (the behavior manual).  
Now it's time to give our new employee a **textbook**.

{: .note }
> When we tested the same questions in M6, we only checked **scope and tone**. In this module, we'll compare whether those same questions now produce **answers based on company documents**.

| State | Analogy | Agent Response |
|:------|:--------|:---------------|
| Instructions only | New employee with only a behavior manual | "I'm unable to provide an accurate answer..." |
| Instructions **+ Knowledge** | New employee with a behavior manual + textbook | "According to the document..." (accurate and specific) |

{: .highlight }
> **The better the textbook, the better the answers.** This is the real-world application of what we learned in M1: "Different ingredients produce different results."

---

## 4 Ways to Connect Knowledge

| Method | Difficulty | Stays Up-to-Date | Access Control | Recommended |
|:-------|:----------|:-----------------|:---------------|:------------|
| **File Upload** ← Today's lab | ⭐ Easy | Manual | ❌ | ✅ **Beginner Step 1** |
| Website URL | ⭐⭐ | Periodic | ❌ | Step 2 |
| SharePoint | ⭐⭐⭐ | Automatic | ✅ | Production |
| Dataverse | ⭐⭐⭐ | Real-time | ✅ | Advanced |

{: .tip }
> Today we start with **File Upload**. It's the easiest and fastest. You can switch to SharePoint when moving to production.

---

## Lab: File Upload

{: .important }
> 📌 This lab is on a separate page.  
> Complete [Lab: File Upload](m07-1-file-upload) and come back here.

---

## Document Authoring Best Practices

For your agent to answer more accurately, **document structure** matters.

| Principle | Description | Example |
|:----------|:------------|:--------|
| **Q&A Format** | Write as question-answer pairs | Q: How many vacation days? A: 15 days |
| **Clear Headings** | Use section headings and subheadings | `## Benefits Points` → `### Where to Use` |
| **Use Tables** | Present structured data in tables | Contact persons, phone numbers, etc. |
| **Short Sentences** | Keep sentences under 50 characters | Prioritize clarity over long sentences |

{: .tip }
> **Structured documents (Q&A / tables) > Narrative documents** — AI answers more accurately from structured information.

---

## Key Takeaways

1. Knowledge = Textbook — **The better the textbook, the better the answers**
2. File Upload is the **easiest and fastest** starting point
3. Documents in **Q&A + table** format work best
4. Verify the impact with Before/After testing

---

## FAQ

| Question | Answer |
|:---------|:-------|
| Can I upload PDFs? | Yes. Word, PDF, TXT, and Excel are all supported. |
| If I replace a file later, will it update automatically? | Manual updates are required. Delete the existing file and upload the new one. |
| Is there a file size limit? | There is a per-file limit. Split large files before uploading. |
| Is it safe to upload confidential documents? | They are used only within Copilot Studio. M365 security policies apply. |

---

## References

| Resource | Link |
|:---------|:-----|
| Connecting Knowledge Sources | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/knowledge-copilot-studio) |
| File Upload Knowledge Source | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/knowledge-add-file-upload) |
| Knowledge Document Best Practices | [learn.microsoft.com](https://learn.microsoft.com/microsoft-copilot-studio/guidance/building-agents-knowledge) |

---

Next module: [M8. Element 4 — Tools](m08-tools-overview)
