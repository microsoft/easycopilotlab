---
title: "Lab ② — Change Agent Settings"
parent: "M5. Component 1 — Orchestrator & AI"
nav_order: 2
---

# Lab ②: Change Agent Settings
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 11:20 | 10 min | 🟢 Hands-on lab |

---

In this lab, you'll **pre-configure the agent's Generative AI settings** so that labs in later modules work smoothly.

## Step 1 — Open the Settings Screen

1. Copilot Studio → Open the HR Assistant agent
2. Click the **⚙️ Settings** button in the **top right** of the agent screen
3. Select **Generative AI** from the left menu

---

## Step 2 — Configure Each Setting

Review and update each setting in the order shown below:

| # | Setting | Value | Description |
|:--|:--------|:-----:|:------------|
| 1 | **Orchestration** | **Yes** (verify) | Allows the agent to automatically select the best tool among Knowledge, Topics, and Flows. If turned off, the agent cannot use any tools at all. |
| 2 | **Connected agents** | **On** (verify) | Must be enabled for the M14 Multi-Agent lab where agents collaborate with each other. |
| 3 | **Response** | **Keep as-is** | It's more effective to control response length and format through Instructions (M6) using text. |
| 4 | **Moderation** | **Low** | This is the content filtering level. Setting it to "High" may block legitimate responses, so "Low" is more suitable during labs. |
| 5 | **User feedback** | **Off** | This shows 👍👎 buttons after each response. Not needed for labs, so turn it off. |
| 6 | **File upload** | **Off** | Allows users to attach files during conversations. This is separate from connecting files as knowledge sources in M7. Turn it off for labs. |
| 7 | **Code interpreter** | **Off** | Enables Python code execution. Not needed for an HR Assistant, so turn it off. |
| 8 | **Turn on Actions IQ** | **On** | Enables the agent to automatically recognize Power Automate flows as tools. Required for the M12 Agent Flow lab. |

{: .note }
> You don't need to fully understand what each setting does right now. You'll naturally grasp them as you use these features in later modules.

---

## Step 3 — Save and Close

1. Click the **"Save"** button at the bottom of the settings screen
2. Once saved, click the **"✕"** in the top right to close settings and return to the agent

---

## Settings Summary

| Setting | Value | Related Module |
|:--------|:-----:|:---------------|
| Orchestration | Yes | All (auto tool selection) |
| Connected agents | On | M14 Multi-Agent |
| Moderation | Low | All (relaxed filtering) |
| Actions IQ | On | M12 Agent Flow |
| User feedback | Off | — |
| File upload | Off | — |
| Code interpreter | Off | — |

{: .important }
> These settings form the **foundation for all subsequent labs**. If the agent behaves unexpectedly during a lab, check these settings first.

---

Once you've completed the lab, [return to the M5 main page](m05-orchestrator).
