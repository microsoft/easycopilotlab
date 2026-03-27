# 모듈별 삽화 이미지 생성 프롬프트

> **스타일 공통 지시문 (모든 프롬프트 앞에 붙이세요)**
>
> ```
> Style: Flat vector illustration, warm pastel color palette (soft blue, coral, cream, mint), 
> clean lines, minimal detail, friendly and approachable. 
> Consistent character: a cheerful young AI office worker (gender-neutral, wearing a name tag 
> that says "AI 신입", slightly robotic but cute features — like small antenna or LED eyes). 
> Korean office setting. No text in the image. 16:9 aspect ratio, suitable as a web page header banner.
> ```

---

## M0. 오리엔테이션 — 오늘 만들 에이전트 미리보기

**파일명:** `assets/images/m00/hero.png`

```
The AI rookie employee stands at the entrance of a modern Korean office, wearing a 
brand-new name tag. A senior office worker welcomes them with a handshake. Behind them, 
a glass whiteboard shows a simple roadmap with 7 milestone icons (lightbulb → document → 
book → wrench → rocket → gears → star). The mood is "first day at work, full of 
possibilities." Morning sunlight streams through the windows.
```

---

## M1. 동작원리 — 당신은 AI와 대화하고 있지 않다

**파일명:** `assets/images/m01/hero.png`

```
Center of the image: a large, prominent traffic controller / orchestrator character 
(a friendly robot wearing a dispatcher headset and a vest labeled with a gear icon) 
stands between a human user on the LEFT and a glowing LLM brain on the RIGHT. 

The orchestrator holds a clipboard (system prompt) in one hand. With the other hand, 
it directs multiple actions simultaneously — like an air traffic controller: 
(1) reading a document/file, (2) searching the web with a magnifying glass on a globe, 
(3) running code on a small screen showing brackets, (4) generating an image on a canvas, 
(5) pulling data from email/calendar icons.

Crucially, there is NO direct line between the human and the LLM brain. ALL arrows 
go THROUGH the orchestrator. The human speaks to the orchestrator, the orchestrator 
gathers and processes, then passes everything to the LLM, and returns the answer.

The mood is "revelation — you thought you were talking to the brain, but actually 
the dispatcher runs the show." The AI rookie character watches from behind the 
orchestrator, learning the truth.
```

### M1 인포그래픽 ① — 오케스트레이터 구조도

**파일명:** `assets/images/m01/orchestrator-flow.png`

```
Clean infographic diagram on a white/light gray background. Top-down vertical flow.

TOP: A person icon labeled "사용자 질문" inside a rounded rectangle.
Arrow pointing DOWN to:

MIDDLE (largest element, highlighted): A bold dark blue (#1a3a5c) rounded rectangle 
labeled "🚦 오케스트레이터" with a gradient from dark navy to bright blue (#2563eb). 
Inside this box, two sub-layers are visible:

  Layer 1: A light blue (#e8eef6) banner reading "📋 시스템 프롬프트 — 목적 · 태도 · 제한사항"
  
  Layer 2: A row of 6 equally-sized rounded cards in light blue (#e8eef6) with thin 
  blue (#2563eb) borders, each showing an icon and short Korean label:
    📎 첨부파일 읽기 | 🔍 웹 검색 | 🎨 이미지 생성 | 🐍 코드 실행 | 📧 메일·파일·일정 | 💬 대화 기록

Arrow pointing DOWN to:

BOTTOM-LEFT: A light rounded rectangle "🧠 LLM"
Arrow pointing DOWN to:
BOTTOM: A rounded rectangle "💬 답변"

IMPORTANT: There must be NO direct arrow from the person to the LLM. Everything flows 
THROUGH the orchestrator box. The orchestrator box should be visually dominant — at least 
3x the size of other elements. Use the color palette: #1a3a5c (dark navy), #2563eb (blue), 
#e8eef6 (light blue), #f7f9fc (near-white), #cbd5e0 (gray border). 
No text other than labels. Flat vector style, 16:9 aspect ratio.
```

### M1 인포그래픽 ② — 같은 LLM, 다른 오케스트레이터

**파일명:** `assets/images/m01/orchestrator-compare.png`

```
Clean infographic comparing three AI services side by side. White background, 16:9.

THREE COLUMNS, equally spaced:

COLUMN 1 — "ChatGPT" (gray theme #6b7280):
  Top: person icon → arrow down →
  Middle: gray rounded rectangle "🚦 범용 오케스트레이터" with sub-text 
  "웹검색 · 코드실행 · 이미지생성"
  Below: small text "📋 범용 AI 어시스턴트" and "🗂 사용자가 직접 제공"

COLUMN 2 — "Copilot" (blue theme #2563eb):
  Top: person icon → arrow down →
  Middle: blue rounded rectangle "🚦 M365 오케스트레이터" with sub-text 
  "업무특화 · M365데이터 · 웹검색"
  Below: small text "📋 M365 업무 도우미" and "🗂 이메일 · 파일 · 일정 · Teams"

COLUMN 3 — "우리 에이전트" (dark navy theme #1a3a5c, with a star badge, 
  slightly larger/emphasized with a subtle drop shadow):
  Top: person icon → arrow down →
  Middle: dark navy-to-blue gradient rounded rectangle "🚦 우리가 만든 오케스트레이터" 
  with sub-text "HR특화 · 사내규정 · 커넥터 · 흐름"
  Below: small text "📋 HR 전문 도우미" and "🗂 사내규정 · Excel · 커넥터"

ALL THREE columns have arrows converging DOWN to a single shared element at the bottom:
  A light rounded rectangle "🧠 같은 GPT-5 엔진"

Below that, a single line caption: "LLM은 같다. 오케스트레이터가 다르면 결과가 다르다."

Flat vector style, consistent with the orchestrator-flow image. Same color palette.
```

---

## M2. 몰입형 vs 인컨텍스트

**파일명:** `assets/images/m02/hero.png`

```
Split scene illustration. LEFT side: The AI rookie sits at a dedicated consultation desk 
(like a bank teller window) having a focused 1-on-1 conversation with a user — a sign says 
"전용 창구" (dedicated counter). RIGHT side: The same AI rookie pops up from behind a 
colleague's desk as a small hologram, answering a quick question while the colleague 
continues typing — casual, quick interaction. A dotted line divides the two scenes. 
Both scenarios show the same AI rookie character.
```

---

## M3. 첫번째 에이전트 — 에이전트 빌더 실습

**파일명:** `assets/images/m03/hero.png`

```
The AI rookie is being "assembled" on a conveyor belt in a friendly toy factory. A human 
office worker presses a single large button labeled with a sparkle icon. The AI rookie, 
freshly created, stands up with a cheerful expression but with an empty backpack (no 
knowledge yet). Surrounding shelves show empty slots where textbooks and tools will go 
later. The mood is quick and simple — "30 seconds to create."
```

---

## M3a. 샘플 에이전트 체험

**파일명:** `assets/images/m03a/hero.png`

```
Six small AI rookie clones, each wearing a different costume: one in a referee outfit 
(roleplay trainer), one with a giant pencil (writing coach), one at a debate podium 
(expert panel), one holding a clipboard (meeting notes), one with an envelope (email 
writer), one with an interview microphone (interview question generator). They all stand 
in a line on a stage like characters at a theme park meet-and-greet. Colorful and playful.
```

---

## M4. 4가지 구성요소

**파일명:** `assets/images/m04/hero.png`

```
An exploded/blueprint diagram of the AI rookie character, shown as four detachable parts 
like a toy figure assembly guide: (1) HEAD = engine/brain icon (orchestrator), (2) CHEST = 
a document/job posting pinned to it (instructions), (3) BACKPACK = filled with books 
(knowledge), (4) HANDS & FEET = tools like wrench, phone, envelope (tools). Each part 
floats slightly apart with dotted lines showing where they connect. Clean, technical-yet-cute.
```

---

## M5. 오케스트레이터

**파일명:** `assets/images/m05/hero.png`

```
The AI rookie sits in the driver's seat of a friendly-looking car. The dashboard shows 
an "AUTO" mode switch (glowing green) and a "MANUAL" switch (grayed out). Through the 
windshield, a road with multiple forking paths is visible — each path has a small icon: 
book, chat bubble, gear. The AI rookie looks confident with hands on the wheel. The metaphor: 
"automatic transmission — the AI drives itself, choosing the right path."
```

---

## M6. 지침

**파일명:** `assets/images/m06/hero.png`

```
A human manager stands at a desk holding a large document titled with a checklist icon 
(the job posting). The AI rookie stands across the desk, eagerly receiving the document. 
The document has four visible sections highlighted in different colors: a person icon 
(role), a boundary icon (scope), a speech bubble (attitude), and a shield icon (principles). 
The mood is "new hire orientation meeting." An office setting with warm lighting.
```

---

## M7. 지식

**파일명:** `assets/images/m07/hero.png`

```
The AI rookie sits at a desk with an empty backpack open in front of them. A human 
colleague is loading colorful textbooks into the backpack — each book spine shows a 
simple icon: FAQ, person/contact, heart/benefits, receipt/expenses, calendar/vacation. 
A before/after split: LEFT side the AI rookie has question marks floating above (confused), 
RIGHT side (after receiving books) the AI rookie has lightbulbs and checkmarks (confident). 
```

---

## M8. 도구들

**파일명:** `assets/images/m08/hero.png`

```
The AI rookie stands in a workshop/toolshed. On a pegboard wall behind them, various 
tools hang neatly, each with a small label icon: a script/clapperboard (Topic), a plug 
(connector), a flow/river diagram (agent flow), a sparkle-brain (AI prompt), two figures 
shaking hands (multi-agent), a globe with a plug (MCP), an alarm bell (trigger). The AI 
rookie is reaching for one of the tools with an eager expression. "Choosing the right 
tool for the job."
```

---

## M9. 토픽과 변수

**파일명:** `assets/images/m09/hero.png`

```
The AI rookie is on a small theater stage, holding a movie clapperboard (Topic = script). 
On a large cork board next to the stage, several colorful sticky notes (post-it notes = 
variables) are pinned, with arrows connecting them. One sticky note says a person icon, 
another shows a phone icon. The AI rookie reads from the clipboard and checks a sticky 
note. The metaphor: "following a script, with post-it memos to remember things."
```

---

## M10. 게시와 공유

**파일명:** `assets/images/m10/hero.png`

```
The AI rookie stands on a launch pad, like a small rocket ready for takeoff. A human 
presses a big green "PUBLISH" button. In the sky above, icons of different platforms 
float like clouds: a Teams logo-like icon, a globe (website), a chat bubble (Copilot). 
Confetti and streamers suggest celebration. The mood: "launch day — going live!" 
Another human waves from a separate desk, receiving a "share" notification.
```

---

## M11. 커넥터

**파일명:** `assets/images/m11/hero.png`

```
The AI rookie sits at a desk writing in a diary/journal (auto-logging). A glowing cable 
runs from the AI rookie's desk directly to a large Excel spreadsheet floating nearby. 
Each time the AI rookie talks (speech bubbles), a new row automatically appears on the 
spreadsheet. The metaphor: "the AI keeps a diary automatically." The Excel sheet shows 
neat rows filling up. Simple, one direct connection — a single cable, not complex wires.
```

---

## M12. 에이전트 흐름

**파일명:** `assets/images/m12/hero.png`

```
The AI rookie is working on an assembly line / conveyor belt. Three stations are visible: 
(1) collecting information into a clipboard, (2) a small AI brain generating an email 
draft on screen, (3) an envelope sliding into a mailbox. The conveyor belt connects all 
three stations with arrows. The metaphor: "multi-step automation — information flows 
through stages." The AI rookie supervises the whole line proudly.
```

---

## M13. AI 프롬프트

**파일명:** `assets/images/m13/hero.png`

```
A Power Automate flow diagram shown as a simple pipe/plumbing system. In the middle of 
the pipes, one section glows with a sparkle/brain icon (the AI prompt). Input goes in 
as plain text (a document), and output comes out transformed: categorized, summarized, 
or translated. Four small vignettes around the pipe show: text (classification), an eye 
viewing a receipt (multimodal), code brackets (code interpreter), and a Word document 
icon (Word output). The AI rookie watches this transformation happen.
```

---

## M14. 멀티에이전트

**파일명:** `assets/images/m14/hero.png`

```
A reception desk scene: A "Super Host" AI character (wearing a concierge uniform with 
a star badge) stands behind a front desk. Two doors behind the concierge are labeled 
with icons: one with a heart (HR) and one with a gavel/scale (Legal). A user approaches 
the front desk with a question. The concierge gestures toward the appropriate door. 
The metaphor: "a hotel concierge directing guests to the right specialist." 
Each specialist agent peeks out from their door.
```

---

## M15. MCP

**파일명:** `assets/images/m15/hero.png`

```
The AI rookie stands in front of a universal power adapter / multi-port hub. Various 
external service icons (a search magnifying glass, a stock chart, a news icon, a map pin) 
are plugged into the hub via standardized cables. All cables are identical (standardized 
protocol). The AI rookie connects one cable and suddenly multiple tool icons light up. 
The metaphor: "one universal adapter connects to everything." A globe in the background 
suggests external/worldwide services.
```

---

## M16. 트리거

**파일명:** `assets/images/m16/hero.png`

```
The AI rookie is sleeping at a desk (peace signs, "zzz" floating). Suddenly, an alarm 
bell rings — triggered by a form submission (a paper airplane flying in from outside). 
The AI rookie wakes up instantly, catches the paper airplane, reads it, writes a draft 
reply, and hands it to a human colleague for review. The metaphor: "the AI wakes up 
automatically when an event happens, but a human makes the final call." Split into 
three mini-moments: sleeping → triggered → human reviews.
```

---

## M17. 마무리

**파일명:** `assets/images/m17/hero.png`

```
A graduation/completion scene. The AI rookie (now with a small graduation cap) stands 
proudly next to the human office worker who created it. Behind them, a wall display 
shows all the components assembled: the job posting (instructions), textbooks (knowledge), 
tools, scripts (topics), and connections. A banner says nothing (no text) but has 
celebratory elements: confetti, a trophy, checkmarks. The mood is warm and accomplished. 
A small roadmap arrow points forward (suggesting "next steps").
```
