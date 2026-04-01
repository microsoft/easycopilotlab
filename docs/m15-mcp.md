---
title: "M15. Tools — MCP"
nav_order: 16
has_children: true
---

# Advanced Tools — MCP
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 17:10 | 15 min | 🟢 Hands-on Lab |

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

![M15 MCP — Connect to External Services with One Universal Adapter](../assets/images/m15/hero.png)

---

## What You'll Learn in This Module

- What **MCP (Model Context Protocol)** is
- How to connect an MCP server to an agent in Copilot Studio
- Hands-on lab connecting the **Naver Search MCP** and **Stock Price MCP** provided by the instructor

{: .highlight }
> MCP is a protocol that connects external services to agents in a standardized way. By connecting a single MCP server, the agent can use all of that service's capabilities as tools.

---

## What Is MCP?

**Model Context Protocol** is a standard specification that allows AI models to communicate with external services and tools.

| Traditional Approach | MCP Approach |
|:---------------------|:-------------|
| Individual setup per connector | Connect dozens of tools via a single MCP server |
| Centered on the Microsoft ecosystem | Can connect to any service |
| Developers must build custom connectors | Ready to use as soon as an MCP server exists |

---

{: .important }
> 👉 [Lab: Connect an MCP Server](m15-1-mcp-connect)

---

## Transition to M16

The instructor can use the following transition:

> We just expanded the **range of tools the agent can use during a conversation** to include external services. In the next module, M16, we'll go one step further and define **conditions that start the agent even without a conversation**. In other words, we're moving beyond what the agent can do and into **when it should act automatically**.

---

## Key Takeaways

1. MCP = a standard protocol for connecting external services as agent tools
2. A single MCP server URL can provide dozens of capabilities at once
3. You can build your own MCP server or use publicly available ones

---

Next module: [M16. Tools — Triggers](m16-trigger)
