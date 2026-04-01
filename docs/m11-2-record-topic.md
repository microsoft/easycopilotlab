---
title: "Lab ② — Record Topic + Excel Connector"
parent: "M11. Tools — Connectors"
nav_order: 2
---

# Lab ②: Connect the Excel Connector in the Record Topic
{: .no_toc }

| Time | Duration | Participant Role |
|:-----|:---------|:-----------------|
| 15:25 | 20 min | 🟢 Hands-on Lab |

---

## Step 1 — Create the Topic + Set the Trigger

1. Copilot Studio → **Topics** → **"+ Add a topic"** → **"From blank"**
2. Topic name: `Record Topic`
3. Click the trigger node → select **"Change trigger"**
4. From the trigger type list, select **"After response"**
   - This means "automatically runs every time the AI generates a response"

{: .highlight }
> A regular Topic's trigger is **"Phrases"**. Because the Record Topic uses an **"After response"** trigger, it **runs automatically every time** — even without the user saying anything specific.

## Step 2 — Add the Excel Connector

5. Click **"+"** below the trigger → select **"Call an action"**
6. Search for **"Excel"** in the connector search bar → select **"Excel Online (Business)"**
7. From the action list, select **"Add a row into a table"**
8. When the connection authorization popup appears, click **"Authorize"** (sign in with your Microsoft 365 account)

## Step 3 — Connect the Excel File + Map Columns

9. Set the configuration fields as follows:

| Field | Value |
|:------|:------|
| Location | **OneDrive for Business** |
| Document Library | (default) |
| File | Select `대화기록.xlsx` |
| Table | Select `Table1` |

10. Column mapping (click the input field to the right of each column → insert variable):

| Excel Column | Mapped Value | Description |
|:-------------|:-------------|:------------|
| Time | `utcNow()` (enter as formula) | Current timestamp |
| User | `System.User.PrincipalName` | Person who asked |
| Question | `System.Activity.Text` | User input |
| Answer | `System.Response.FormattedText` | Agent response |

11. **Save**

{: .tip }
> This Topic is not invoked by the user directly. It's an automatic Topic that "runs every time a response is generated," and it **calls the Excel connector directly** from within.

---

## Test

1. Enter any question in the test panel: **"How many vacation days do I have?"**
2. The agent responds
3. Open **OneDrive → 대화기록.xlsx** → verify that a new row has been added! 🎉

{: .important }
> If you can see the Time, User, Question, and Answer being populated in Excel, you've succeeded.

---

Once you've completed this lab, [return to the M11 main page](m11-connector).
