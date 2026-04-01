---
title: "Lab — Connect an MCP Server"
parent: "M15. Tools — MCP"
nav_order: 1
---

# Lab: Connect an MCP Server
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 17:10 | 10 min | 🟢 Hands-on Lab |

---

## Prerequisites

Have the MCP server URLs provided by the instructor ready:

| MCP Server | Function |
|:-----------|:---------|
| Naver Search MCP | Query Naver news and search results |
| Stock Price MCP | Look up domestic and international stock prices in real time |

## Steps

1. Copilot Studio → Open the HR Assistant (or Super Host) agent
2. Select **Actions → + Add an action → Add MCP server**
3. Enter the **MCP server URL** provided by the instructor
4. Confirm the connection and review the list of available tools
5. Click **Save**
6. Test: Enter "What's the Samsung Electronics stock price?" / "Search today's IT news"

{: .note }
> The MCP server is provided separately by the instructor. You cannot complete this lab without the server URL.

{: .tip }
> The Description matters for MCP tools, too. If you specify in the instructions when the agent should use each tool, the orchestrator will select it more reliably.

---

Once you've completed the lab, [return to the M15 overview](m15-mcp).
