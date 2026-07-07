<!--
author:   Learning & Development Facilitator
email:    ld@yourorganisation.org
version:  3.0.0
language: en-GB
narrator: UK English Female
comment:  Trainer-led AI Competency Assessment Tool — adapted from UNESCO AI Competency Framework LO5.1.2 (Acquire Level). The trainer administers all assessments, scores all responses, identifies gaps, and prescribes targeted development for each participant.
mode:     Textbook

logo: https://cdn-icons-png.flaticon.com/512/8055/8055805.png
icon:     https://cdn-icons-png.flaticon.com/512/8055/8055805.png

script: https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.min.js
link:   https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap

style: |

  /* ── Base ─────────────────────────────────────────── */
  body { font-family: 'Inter', sans-serif; color: #1a1a2e; }

  /* ── Trainer / Phase boxes ────────────────────────── */
  .trainer-banner {
    background: linear-gradient(135deg, #1f5c99 0%, #0d3b6e 100%);
    color: white; border-radius: 10px; padding: 18px 24px; margin: 18px 0;
    box-shadow: 0 4px 16px rgba(31,92,153,0.3);
  }
  .trainer-banner h3, .trainer-banner h4 { color: #f2d06b; margin-top: 0; }

  .phase-header {
    background: linear-gradient(90deg, #0d3b6e, #1f5c99);
    color: white; border-radius: 8px; padding: 14px 20px; margin: 20px 0 10px;
    display: flex; align-items: center; gap: 12px;
  }
  .phase-header .phase-num {
    background: #f2a900; color: #1a1a2e; border-radius: 50%;
    width: 36px; height: 36px; display: flex; align-items: center;
    justify-content: center; font-weight: 800; font-size: 1.1em; flex-shrink: 0;
  }

  /* ── Content boxes ────────────────────────────────── */
  .employee-task {
    background: #eaf3fb; border-left: 6px solid #1f5c99;
    padding: 18px 22px; border-radius: 8px; margin: 16px 0;
  }
  .employee-task h4 { color: #1f5c99; margin-top: 0; }

  .rubric-box {
    background: #fff8e8; border-left: 6px solid #f2a900;
    padding: 18px 22px; border-radius: 8px; margin: 16px 0;
  }
  .rubric-box h4 { color: #b57800; margin-top: 0; }

  .gap-box {
    background: #fdecea; border-left: 6px solid #d93025;
    padding: 18px 22px; border-radius: 8px; margin: 16px 0;
  }
  .gap-box h4 { color: #d93025; margin-top: 0; }

  .prescription-box {
    background: #e9f9ee; border-left: 6px solid #1e8e3e;
    padding: 18px 22px; border-radius: 8px; margin: 16px 0;
  }
  .prescription-box h4 { color: #1e8e3e; margin-top: 0; }

  .tip-box {
    background: #f1ecfb; border-left: 6px solid #6a3fc7;
    padding: 14px 20px; border-radius: 8px; margin: 14px 0;
  }

  .group-box {
    background: linear-gradient(135deg, #fff8e8, #fff3d0);
    border: 2px solid #f2a900; border-radius: 10px;
    padding: 18px 22px; margin: 16px 0;
  }
  .group-box h4 { color: #b57800; margin-top: 0; }

  .individual-box {
    background: linear-gradient(135deg, #eaf3fb, #d6e9f8);
    border: 2px solid #1f5c99; border-radius: 10px;
    padding: 18px 22px; margin: 16px 0;
  }
  .individual-box h4 { color: #1f5c99; margin-top: 0; }

  /* ── Level badges ─────────────────────────────────── */
  .level-grid { display: flex; gap: 10px; flex-wrap: wrap; margin: 14px 0; }
  .level-badge {
    flex: 1; min-width: 130px; border-radius: 8px;
    padding: 12px 14px; font-size: 0.88em; font-weight: 600;
  }
  .l1 { background: #fdecea; border: 2px solid #d93025; color: #d93025; }
  .l2 { background: #fff8e8; border: 2px solid #f2a900; color: #b57800; }
  .l3 { background: #e9f9ee; border: 2px solid #1e8e3e; color: #1e8e3e; }
  .l4 { background: #eaf3fb; border: 2px solid #1f5c99; color: #1f5c99; }

  /* ── Competency type tags ─────────────────────────── */
  .tag {
    display: inline-block; border-radius: 12px; padding: 3px 12px;
    font-size: 0.78em; font-weight: 700; margin: 2px 4px 8px 0;
  }
  .tag-knowledge  { background: #e8f0fe; color: #1a73e8; }
  .tag-skill      { background: #fce8e6; color: #d93025; }
  .tag-attitude   { background: #e6f4ea; color: #1e8e3e; }
  .tag-group      { background: #fff3e0; color: #e65100; }
  .tag-individual { background: #f3e5f5; color: #6a1b9a; }

  /* ── Chip / time indicator ────────────────────────── */
  .time-chip {
    display: inline-block; background: #1f5c99; color: white;
    border-radius: 14px; padding: 4px 16px; font-size: 0.82em;
    margin-bottom: 14px; font-weight: 600;
  }

  /* ── Two-column flex layout ───────────────────────── */
  .two-col { display: flex; gap: 20px; flex-wrap: wrap; margin: 16px 0; }
  .two-col > div { flex: 1; min-width: 260px; }

  /* ── Tables ───────────────────────────────────────── */
  table { width: 100%; border-collapse: collapse; margin: 12px 0; }
  th { background: #1f5c99; color: white; padding: 10px 13px; text-align: left; }
  td { border: 1px solid #ddd; padding: 9px 13px; }
  tr:nth-child(even) td { background: #f5f8fc; }

  /* ── Score matrix table ───────────────────────────── */
  .score-matrix th { background: #0d3b6e; }
  .score-matrix td { text-align: center; font-weight: 600; }
  .score-matrix td:first-child { text-align: left; font-weight: 400; }

  /* ── Progress bar ─────────────────────────────────── */
  .progress-track {
    background: #e0e0e0; border-radius: 8px; height: 12px;
    margin: 6px 0 14px; overflow: hidden;
  }
  .progress-fill {
    height: 100%; border-radius: 8px;
    background: linear-gradient(90deg, #1f5c99, #f2a900);
    transition: width 0.5s ease;
  }

  /* ── Floating avatar ──────────────────────────────── */
  #trainer-avatar-wrap {
    position: fixed; bottom: 24px; right: 24px; z-index: 10000;
    display: flex; flex-direction: column; align-items: flex-end;
  }
  #avatar-bubble {
    background: #1f5c99; color: white; border-radius: 10px 10px 4px 10px;
    padding: 8px 14px; font-size: 11px; max-width: 160px;
    margin-bottom: 8px; text-align: center; display: none;
    box-shadow: 0 2px 10px rgba(0,0,0,0.25); line-height: 1.5;
  }
  #avatar-bubble::after {
    content: ''; position: absolute; bottom: -8px; right: 14px;
    border: 8px solid transparent; border-top-color: #1f5c99;
    border-bottom: 0; margin-left: -4px;
  }
  #avatar-face {
    width: 80px; height: 80px; border-radius: 50%;
    background: white; border: 3px solid #1f5c99;
    box-shadow: 0 4px 20px rgba(0,0,0,0.28);
    cursor: pointer; overflow: hidden;
  }

  /* ── Checklist ────────────────────────────────────── */
  .checklist { list-style: none; padding: 0; }
  .checklist li { padding: 6px 0; display: flex; align-items: flex-start; gap: 10px; }
  .checklist li::before { content: '☐'; font-size: 1.1em; flex-shrink: 0; }

  /* ── Mobile ───────────────────────────────────────── */
  @media (max-width: 640px) {
    .two-col { flex-direction: column; }
    .level-grid { flex-direction: column; }
    #trainer-avatar-wrap { bottom: 12px; right: 12px; }
    #avatar-face { width: 60px; height: 60px; }
  }
-->

# AI Competency Assessment Programme
### Trainer Facilitator Guide — UNESCO LO5.1.2 Acquire Level

---

<!-- Floating animated trainer avatar injected here — runs once on load -->
<script>
(function () {
  if (document.getElementById('trainer-avatar-wrap')) return;

  var wrap = document.createElement('div');
  wrap.id = 'trainer-avatar-wrap';
  wrap.innerHTML = [
    '<div id="avatar-bubble">🎤 Narration playing...</div>',
    '<div id="avatar-face">',
    '<svg viewBox="0 0 100 110" xmlns="http://www.w3.org/2000/svg" width="80" height="80">',
    '<!-- Hair -->',
    '<ellipse cx="50" cy="28" rx="31" ry="16" fill="#3d2b1f"/>',
    '<!-- Head -->',
    '<ellipse cx="50" cy="48" rx="28" ry="30" fill="#f5c99a"/>',
    '<!-- Ears -->',
    '<ellipse cx="22" cy="50" rx="5" ry="7" fill="#f5c99a"/>',
    '<ellipse cx="78" cy="50" rx="5" ry="7" fill="#f5c99a"/>',
    '<!-- Glasses frame -->',
    '<rect x="27" y="38" width="18" height="13" rx="5" fill="none" stroke="#333" stroke-width="2"/>',
    '<rect x="55" y="38" width="18" height="13" rx="5" fill="none" stroke="#333" stroke-width="2"/>',
    '<line x1="45" y1="44" x2="55" y2="44" stroke="#333" stroke-width="2"/>',
    '<line x1="22" y1="44" x2="27" y2="44" stroke="#333" stroke-width="1.5"/>',
    '<line x1="73" y1="44" x2="78" y2="44" stroke="#333" stroke-width="1.5"/>',
    '<!-- Eyes -->',
    '<circle cx="36" cy="44" r="4" fill="#3d2b1f"/>',
    '<circle cx="64" cy="44" r="4" fill="#3d2b1f"/>',
    '<circle cx="37" cy="43" r="1.5" fill="white"/>',
    '<circle cx="65" cy="43" r="1.5" fill="white"/>',
    '<!-- Nose -->',
    '<path d="M 48 52 Q 50 58 52 52" stroke="#d4956a" stroke-width="1.5" fill="none"/>',
    '<!-- Mouth - animated via JS -->',
    '<path id="avatar-mouth" d="M 38 65 Q 50 71 62 65" stroke="#8b4513" stroke-width="2.5" fill="none" stroke-linecap="round"/>',
    '<!-- Body collar -->',
    '<path d="M 15 108 Q 25 88 50 82 Q 75 88 85 108 Z" fill="#1f5c99"/>',
    '<!-- Collar detail -->',
    '<path d="M 50 82 L 43 96 L 50 103 L 57 96 Z" fill="#f2a900"/>',
    '</svg>',
    '</div>'
  ].join('');
  document.body.appendChild(wrap);

  var mouthOpen = false;
  setInterval(function () {
    var mouth  = document.getElementById('avatar-mouth');
    var bubble = document.getElementById('avatar-bubble');
    if (!mouth || !bubble) return;
    var speaking = window.speechSynthesis && window.speechSynthesis.speaking;
    bubble.style.display = speaking ? 'block' : 'none';
    if (speaking) {
      mouthOpen = !mouthOpen;
      mouth.setAttribute('d', mouthOpen
        ? 'M 38 65 Q 50 76 62 65'
        : 'M 38 65 Q 50 68 62 65');
    } else {
      mouth.setAttribute('d', 'M 38 65 Q 50 71 62 65');
    }
  }, 220);
})();
</script>

--{{0}}--
Welcome to the AI Competency Assessment Programme. This guide is addressed entirely to you, the trainer. You administer every assessment, you score every response, and you direct each participant's development based on the evidence you collect today.

<div class="trainer-banner">

### 🧑‍🏫 TRAINER — Programme at a Glance

This is a **trainer-administered diagnostic tool** — not a self-paced module for employees. Your role throughout is to assess, score, identify gaps, and prescribe targeted development.

| Phase | What You Do | Format | Time |
|---|---|---|---|
| **1 — Setup** | Register participants; brief the session | Trainer admin | 5 min |
| **2 — Pre-Assessment** | Administer knowledge, skill & attitude tasks; score | Individual written | 20 min |
| **3 — Group Workshop** | Facilitate group challenge; observe & rate | Group activity | 15 min |
| **4 — Individual Deep Dive** | Probe specific gaps 1-to-1 | Individual verbal/written | 15 min |
| **5 — Gap Mapping** | Enter scores; build competency profiles | Trainer analysis | 10 min |
| **6 — Prescription** | Issue personal development plans | Trainer decision | 10 min |
| **7 — Post-Assessment** | Re-administer; compare before & after | Individual written | 15 min |

</div>

---

## Trainer Navigation

<div class="two-col">
<div>

**Jump to Phase:**

- [Phase 1 — Setup](#phase-1-setup-and-registration)
- [Phase 2 — Pre-Assessment](#phase-2-pre-assessment-diagnostic)
- [Phase 3 — Group Workshop](#phase-3-group-workshop-assessment)
- [Phase 4 — Individual Deep Dive](#phase-4-individual-deep-dive-assessment)

</div>
<div>

**Continue:**

- [Phase 5 — Gap Mapping](#phase-5-competency-gap-mapping)
- [Phase 6 — Prescription](#phase-6-development-prescription)
- [Phase 7 — Post-Assessment](#phase-7-post-assessment-and-verification)
- [Trainer Reference](#trainer-reference-and-resources)

</div>
</div>

---

## The Three Competency Types You Are Assessing

<span class="tag tag-knowledge">📘 KNOWLEDGE</span> What participants **know** — assessed by MCQ, written explanation, scenario Q&A

<span class="tag tag-skill">🔧 SKILL</span> What participants **can do** — assessed by live demonstration, task completion, observation checklist

<span class="tag tag-attitude">💡 ATTITUDE</span> How participants **think and judge** — assessed by ethical scenario, group discussion observation, decision-making

---

## The Four-Point Assessment Scale

<div class="level-grid">
<div class="level-badge l1">🔴 Level 1<br><strong>Novice</strong><br><small>No awareness; major gaps; structured intervention required</small></div>
<div class="level-badge l2">🟡 Level 2<br><strong>Developing</strong><br><small>Partial knowledge; misconceptions present; guided learning needed</small></div>
<div class="level-badge l3">🟢 Level 3<br><strong>Competent</strong><br><small>Sound working knowledge; applies concepts reliably</small></div>
<div class="level-badge l4">🔵 Level 4<br><strong>Advanced</strong><br><small>Critical, applied understanding; ready to mentor peers</small></div>
</div>

--------------------------------------------------------------------------

# Phase 1: Setup and Registration

<span class="time-chip">⏱ 5 minutes — Trainer Only</span>

--{{0}}--
Before any participant enters the room, complete this setup phase. Record all session details and familiarise yourself with the five competency areas you will be assessing.

<div class="phase-header"><div class="phase-num">1</div><div><strong>TRAINER ACTION</strong> — Complete before participants arrive</div></div>

## 1.1 Session Details

**Session Date:** [[ DD / MM / YYYY ]]

**Your Name (Trainer):** [[ Full name ]]

**Department / Team Being Assessed:** [[ Department ]]

**Delivery Mode:**

[(X)] Face-to-face workshop
[( )] Online facilitated (video call)
[( )] Blended

**Number of participants:** [[ Number ]]

---

## 1.2 Participant Register

| # | Full Name | Job Title | Department | Assessment ID |
|---|---|---|---|---|
| 1 | | | | P01 |
| 2 | | | | P02 |
| 3 | | | | P03 |
| 4 | | | | P04 |
| 5 | | | | P05 |

---

## 1.3 Five Competency Areas Under Assessment

| Code | Competency Area | Type | What You Are Looking For |
|---|---|---|---|
| **C1** | AI Foundations | <span class="tag tag-knowledge">KNOWLEDGE</span> | Understanding of what AI is, how generative AI works, what hallucination means |
| **C2** | AI Tool Selection | <span class="tag tag-skill">SKILL</span> | Ability to select the right AI tool for the right professional task |
| **C3** | AI Ethics | <span class="tag tag-attitude">ATTITUDE</span> | Awareness of bias, fairness, transparency; ethical judgement in real scenarios |
| **C4** | Data Protection | <span class="tag tag-knowledge">KNOWLEDGE</span> <span class="tag tag-attitude">ATTITUDE</span> | Understanding of GDPR-relevant data categories; correct protective behaviour |
| **C5** | Output Verification | <span class="tag tag-skill">SKILL</span> <span class="tag tag-attitude">ATTITUDE</span> | Critical evaluation of AI-generated content; verification process and habit |

---

## 1.4 Trainer Preparation Checklist

<ul class="checklist">
<li>Participant task sheets printed or shared digitally (one per person)</li>
<li>Group scenario cards prepared (Phase 3)</li>
<li>Scoring sheets ready for each participant</li>
<li>This LiaScript guide open and accessible throughout</li>
<li>Participants briefed that this is an assessment, not a course — they should answer from current knowledge</li>
</ul>

--------------------------------------------------------------------------

# Phase 2: Pre-Assessment Diagnostic

<span class="time-chip">⏱ 20 minutes — Trainer Administered</span>

--{{0}}--
Distribute the participant task sheet. Allow participants to work individually and in silence. Your role here is to observe, circulate, and take notes — not to teach or hint. Score each response using the rubric immediately below each task.

<div class="phase-header"><div class="phase-num">2</div><div><strong>PRE-ASSESSMENT</strong> — Three task types: Knowledge · Skill · Attitude</div></div>

---

## TASK A — Knowledge Assessment (C1 + C4)

<span class="tag tag-knowledge">📘 KNOWLEDGE</span> <span class="tag tag-individual">INDIVIDUAL</span>

<div class="employee-task">

### 📋 Participant Task A

**Answer these questions in your own words. Write what you currently know — there are no trick questions.**

**A1.** In one or two sentences, what is "Artificial Intelligence"?

[[ _____ ]]

**A2.** What is a "hallucination" in AI? Give a workplace example.

[[ _____ ]]

**A3.** You are preparing an HR report and paste employee salary data into ChatGPT. What is the risk?

[[ _____ ]]

**A4.** Name ONE category of data that must never be entered into a general-purpose AI tool.

[[ _____ ]]

</div>

<div class="rubric-box">

### 🧑‍🏫 TRAINER RUBRIC — Task A

| Level | What This Response Looks Like |
|---|---|
| 🔴 **1 — Novice** | Cannot define AI; unaware of hallucination; sees no risk in pasting salary data; cannot name a protected category |
| 🟡 **2 — Developing** | Vague AI definition ("it thinks like a human"); knows hallucination exists but cannot explain it; vaguely says "it's probably not safe" but no reason |
| 🟢 **3 — Competent** | Accurate AI definition referencing patterns or prediction; correctly defines hallucination; identifies data privacy risk; names a relevant protected category (salary, health, performance) |
| 🔵 **4 — Advanced** | Articulates generative vs. traditional AI; explains hallucination with a specific HR consequence; references GDPR or organisational policy; names multiple special-category data types |

**C1 Score for this participant:** [[ 1 / 2 / 3 / 4 ]]

**C4 Score for this participant:** [[ 1 / 2 / 3 / 4 ]]

**Observation note:** [[ What stood out in their response? ]]

</div>

---

## TASK B — Skill Assessment: Tool Selection (C2)

<span class="tag tag-skill">🔧 SKILL</span> <span class="tag tag-individual">INDIVIDUAL</span>

<div class="employee-task">

### 📋 Participant Task B

**B1. Match each AI tool to its correct use. Draw a line or write the letter.**

| AI Tool | Your Answer |
|---|---|
| ChatGPT | |
| Consensus | |
| Microsoft Copilot | |
| Perplexity AI | |

**Options:**

- **A** — Peer-reviewed academic research with citable sources
- **B** — Drafting, summarising, and brainstorming
- **C** — Productivity in Word, Excel, Teams, and Outlook
- **D** — Web search with sourced, linked answers

---

**B2. Scenario:** Your manager asks for a training policy backed by credible research. You have 30 minutes.

Which tool do you use, and why? Write your answer in 2–3 sentences.

[[ _____ ]]

---

**B3.** Name one AI tool you have never used but think could improve your work. What would you use it for?

[[ _____ ]]

</div>

<div class="rubric-box">

### 🧑‍🏫 TRAINER RUBRIC — Task B

**Correct matches:** ChatGPT → B | Consensus → A | Copilot → C | Perplexity → D

| Level | What This Response Looks Like |
|---|---|
| 🔴 **1 — Novice** | All tools confused; believes ChatGPT is the only AI tool; cannot justify any scenario choice |
| 🟡 **2 — Developing** | 1–2 correct matches; scenario picks ChatGPT without considering evidence quality; B3 blank or vague |
| 🟢 **3 — Competent** | 3–4 correct matches; scenario correctly identifies Consensus and explains citations; B3 shows awareness of more than one tool |
| 🔵 **4 — Advanced** | All correct; scenario compares Consensus vs Perplexity and explains why peer-reviewed evidence is needed for policy; B3 response is specific and strategic |

**C2 Score:** [[ 1 / 2 / 3 / 4 ]]

**Observation note:** [[ _____ ]]

</div>

---

## TASK C — Attitude Assessment: Ethics (C3 + C5)

<span class="tag tag-attitude">💡 ATTITUDE</span> <span class="tag tag-individual">INDIVIDUAL</span>

<div class="employee-task">

### 📋 Participant Task C

**C1. Read each statement. Circle TRUE or FALSE and write one sentence explaining your thinking.**

---

*"An AI tool that sounds confident is probably correct."*

[( )] TRUE     [( )] FALSE

Reason: [[ _____ ]]

---

*"AI recruitment tools can contain bias because they were trained on historical hiring data."*

[( )] TRUE     [( )] FALSE

Reason: [[ _____ ]]

---

*"Employees should be told when AI was involved in a decision that affected them."*

[( )] TRUE     [( )] FALSE

Reason: [[ _____ ]]

---

**C2. Verification scenario:**

An AI tool provides this for your HR policy document:

> *"The UK Workplace AI Regulation Act (2023) requires all organisations with over 50 employees to conduct annual AI ethics audits."*

What do you do before including this in your policy? Write step by step.

[[ _____ ]]

</div>

<div class="rubric-box">

### 🧑‍🏫 TRAINER RUBRIC — Task C

**Correct answers:** Statement 1 = FALSE | Statement 2 = TRUE | Statement 3 = TRUE

*(Trainer note: The "Workplace AI Regulation Act 2023" does NOT exist — it is a hallucinated output. A competent participant will attempt to verify it.)*

| Level | What This Response Looks Like |
|---|---|
| 🔴 **1 — Novice** | Multiple wrong answers; would include the hallucinated legislation without checking; no awareness of verification need |
| 🟡 **2 — Developing** | 1–2 correct; says they would "Google it" but has no structured process; does not identify legal risk |
| 🟢 **3 — Competent** | All correct with adequate reasoning; checks legislation.gov.uk or GOV.UK; identifies hallucination and reputational risk |
| 🔵 **4 — Advanced** | All correct with precise legal reasoning; cross-references multiple authoritative sources; articulates liability for publishing false regulatory information in a policy document |

**C3 Score:** [[ 1 / 2 / 3 / 4 ]]

**C5 Score:** [[ 1 / 2 / 3 / 4 ]]

**Observation note:** [[ _____ ]]

</div>

---

## Phase 2 — Trainer Rating Matrix

<div class="trainer-banner">

### Rate Each Participant Across All Five Competencies (1–4)

Use the scores from Tasks A, B, and C above to complete this matrix now. You will use these scores in Phase 5 for gap mapping.

</div>

**Enter scores in the table below:**

[[1 — Novice][2 — Developing][3 — Competent][4 — Advanced]]
[P01: Participant 1] C1 AI Foundations score
[P01: Participant 1] C2 Tool Selection score
[P01: Participant 1] C3 Ethics score
[P01: Participant 1] C4 Data Privacy score
[P01: Participant 1] C5 Verification score

[[1 — Novice][2 — Developing][3 — Competent][4 — Advanced]]
[P02: Participant 2] C1 AI Foundations score
[P02: Participant 2] C2 Tool Selection score
[P02: Participant 2] C3 Ethics score
[P02: Participant 2] C4 Data Privacy score
[P02: Participant 2] C5 Verification score

[[1 — Novice][2 — Developing][3 — Competent][4 — Advanced]]
[P03: Participant 3] C1 AI Foundations score
[P03: Participant 3] C2 Tool Selection score
[P03: Participant 3] C3 Ethics score
[P03: Participant 3] C4 Data Privacy score
[P03: Participant 3] C5 Verification score

--------------------------------------------------------------------------

# Phase 3: Group Workshop Assessment

<span class="time-chip">⏱ 15 minutes — Trainer Facilitated</span>

--{{0}}--
This phase moves from individual written tasks to observed group activity. You are watching how participants reason together, challenge each other, and make collective decisions under ethical pressure. This reveals attitudes and skill application that written tasks sometimes miss.

<div class="phase-header"><div class="phase-num">3</div><div><strong>GROUP WORKSHOP</strong> — Observed collaborative assessment</div></div>

<div class="trainer-banner">

### 🧑‍🏫 TRAINER INSTRUCTION

Divide participants into groups of 3–5. Each group receives one of the three challenges below. After 8 minutes of group discussion, each group presents their decision and reasoning. You assess **individuals** based on what you observe — not the group as a whole.

**What to watch for:**
- Who speaks up about ethical concerns?
- Who defaults to "use ChatGPT" without considering alternatives?
- Who asks about data privacy unprompted?
- Who challenges an incorrect claim from a peer?

</div>

---

## Group Challenge 1 — Recruitment Scenario

<span class="tag tag-group">GROUP</span> <span class="tag tag-attitude">ATTITUDE + KNOWLEDGE</span>

<div class="group-box">

### 📋 Group Task 1

> **Your HR team is under pressure to shortlist 300 job applications in 48 hours. A colleague suggests: "Let's upload all CVs to ChatGPT and ask it to rank the top 50 candidates."**

As a group, discuss and agree:

1. What are the **risks** of doing this?
2. Is there a **better AI approach** that is safer and more defensible?
3. What **policy or principle** should guide your decision?
4. Present your group's recommendation in 2 minutes.

</div>

<div class="rubric-box">

### 🧑‍🏫 TRAINER OBSERVATION — Group Challenge 1

**Watch for and record against each individual:**

| Observation | Who demonstrated this? |
|---|---|
| Raised data privacy concern unprompted | |
| Identified bias risk in AI recruitment | |
| Suggested Consensus or a safer alternative | |
| Referenced organisational policy or GDPR | |
| Challenged a peer's incorrect assumption | |
| Defaulted to "just use ChatGPT" without reflection | |

**Individual attitude scores adjusted based on group observation:**

P01 C3 adjustment: [[ Increase / Decrease / No change ]]

P02 C3 adjustment: [[ Increase / Decrease / No change ]]

P03 C3 adjustment: [[ Increase / Decrease / No change ]]

</div>

---

## Group Challenge 2 — Tool Selection Battle

<span class="tag tag-group">GROUP</span> <span class="tag tag-skill">SKILL</span>

<div class="group-box">

### 📋 Group Task 2

> **Your team has four upcoming tasks. You have four AI tools available: ChatGPT, Consensus, Copilot, and Perplexity. As a group, assign the best tool to each task — and justify your choice.**

| Task | Best AI Tool | Your Justification |
|---|---|---|
| Write a first draft of the induction schedule | | |
| Find peer-reviewed research on hybrid working | | |
| Summarise last month's team performance data in Excel | | |
| Find the latest UK government guidance on flexible working rights | | |

**Group rule:** You must reach unanimous agreement. If you disagree, debate it — the trainer wants to hear the reasoning.

</div>

<div class="rubric-box">

### 🧑‍🏫 TRAINER OBSERVATION — Group Challenge 2

**Correct answers:** Draft → ChatGPT | Research → Consensus | Excel data → Copilot | Government guidance → Perplexity

**Record which individuals drove correct reasoning vs. which followed along:**

Who correctly argued for Consensus for research? [[ Names ]]

Who incorrectly defaulted to ChatGPT for everything? [[ Names ]]

Who understood Copilot's integration purpose? [[ Names ]]

**C2 score adjustment based on group discussion quality:**

P01: [[ Increase / Decrease / No change ]]

P02: [[ Increase / Decrease / No change ]]

P03: [[ Increase / Decrease / No change ]]

</div>

---

## Group Challenge 3 — Ethics Tribunal

<span class="tag tag-group">GROUP</span> <span class="tag tag-attitude">ATTITUDE</span>

<div class="group-box">

### 📋 Group Task 3

> **An HR manager used AI to generate individual employee performance summaries. Employees were not told. The AI tool made several factual errors that affected promotion decisions.**

Your group acts as an **ethics review panel**. Discuss and present:

1. What **ethical principles** were violated?
2. What **harm** was done — to individuals and the organisation?
3. What **three policies** should be introduced to prevent this happening again?
4. One member of the group must argue **devil's advocate** — what might have seemed reasonable about the manager's decision at the time?

</div>

<div class="rubric-box">

### 🧑‍🏫 TRAINER OBSERVATION — Group Challenge 3

**Ethical principles a Competent/Advanced participant should identify:**

- Transparency (employees not informed AI was used)
- Fairness (AI errors affecting career outcomes)
- Human oversight (AI making decisions without verification)
- Data protection (performance data processed without documented lawful basis)
- Accountability (no audit trail)

**Record against each individual:**

| Participant | Principles Named | Depth of Reasoning | Devil's Advocate Quality |
|---|---|---|---|
| P01 | | | |
| P02 | | | |
| P03 | | | |

**C3 final scores after group observation:**

P01: [[ 1 / 2 / 3 / 4 ]]

P02: [[ 1 / 2 / 3 / 4 ]]

P03: [[ 1 / 2 / 3 / 4 ]]

</div>

--------------------------------------------------------------------------

# Phase 4: Individual Deep Dive Assessment

<span class="time-chip">⏱ 15 minutes — 1-to-1 with Trainer</span>

--{{0}}--
Use this phase to probe the gaps you identified in Phases 2 and 3. This is a short one-to-one conversation or individual written task, targeted at each person's weakest competency area. You do not run the same task for everyone — you tailor it to where the gap is.

<div class="phase-header"><div class="phase-num">4</div><div><strong>INDIVIDUAL DEEP DIVE</strong> — Gap-targeted probing by the trainer</div></div>

<div class="trainer-banner">

### 🧑‍🏫 TRAINER INSTRUCTION

After reviewing Phase 2 scores and Phase 3 observations, select **one deep-dive task per participant** based on their weakest area. You run this as a short verbal or written probe — 3–5 minutes per person.

</div>

---

## Deep Dive — C1: AI Foundations (for Novice / Developing)

<span class="tag tag-knowledge">📘 KNOWLEDGE</span> <span class="tag tag-individual">INDIVIDUAL</span>

<div class="individual-box">

### 📋 Verbal Probe — Ask these questions aloud

**Question 1:** Can you explain, in plain English, how ChatGPT produces an answer when you type a question?

**Question 2:** If ChatGPT produces a wrong answer, whose fault is it — the tool, the developer, or the user?

**Question 3:** What is the difference between traditional software (like Excel) and a generative AI tool?

**Listen for:** does the participant understand that AI generates *probabilistic predictions* rather than looking things up? Do they understand that the user is responsible for verifying outputs?

</div>

<div class="rubric-box">

### 🧑‍🏫 SCORING — C1 Deep Dive

| Level | Response Indicators |
|---|---|
| 🔴 **1** | Cannot explain; uses terms like "it searches the internet" or "it knows everything" |
| 🟡 **2** | Understands AI generates text but cannot explain the probabilistic or statistical basis |
| 🟢 **3** | Accurately describes AI as predicting likely outputs based on training data; assigns user responsibility for verification |
| 🔵 **4** | Explains transformer models or training data in accessible terms; discusses the limitation of training cutoff dates; compares generative vs. retrieval-based AI |

Revised C1 score: [[ 1 / 2 / 3 / 4 ]]

</div>

---

## Deep Dive — C2: Tool Selection (for Novice / Developing)

<span class="tag tag-skill">🔧 SKILL</span> <span class="tag tag-individual">INDIVIDUAL</span>

<div class="individual-box">

### 📋 Live Demonstration Task

**Give the participant access to Consensus (consensus.app) and ChatGPT (chat.openai.com).**

Ask them to: *"Find three credible sources supporting the claim that remote working improves productivity."*

Instruct them to use **whichever tool they think is better** — and explain their choice before they begin.

**Observe:** Which tool do they open first? Do they evaluate source quality? Do they check whether citations are real?

</div>

<div class="rubric-box">

### 🧑‍🏫 SCORING — C2 Deep Dive

| Level | Observed Behaviour |
|---|---|
| 🔴 **1** | Opens ChatGPT; accepts generated "sources" without checking; does not use Consensus at all |
| 🟡 **2** | Opens ChatGPT; may find real sources but cannot explain why Consensus would be more reliable |
| 🟢 **3** | Opens Consensus; retrieves peer-reviewed sources; can explain the difference in output quality |
| 🔵 **4** | Uses both tools strategically; explains when ChatGPT is sufficient vs. when citable evidence is required; checks DOI or journal credibility |

Revised C2 score: [[ 1 / 2 / 3 / 4 ]]

</div>

---

## Deep Dive — C3: Ethics (for Novice / Developing)

<span class="tag tag-attitude">💡 ATTITUDE</span> <span class="tag tag-individual">INDIVIDUAL</span>

<div class="individual-box">

### 📋 Scenario Response — Written or Verbal

**Present this scenario:**

> Your organisation is piloting an AI tool that scores job applications before a human sees them. The vendor says the algorithm is "neutral and objective." Three months in, your diversity data shows a steep decline in shortlisting of candidates from two protected groups.

**Ask:**

1. Is the vendor's claim that the tool is "neutral" credible? Why or why not?
2. What should you do as the HR professional responsible for this process?
3. What does "transparency" require you to do — both internally and with candidates?

</div>

<div class="rubric-box">

### 🧑‍🏫 SCORING — C3 Deep Dive

| Level | Response Indicators |
|---|---|
| 🔴 **1** | Accepts "neutral and objective" claim; has no plan; does not see a problem with the diversity data pattern |
| 🟡 **2** | Senses something is wrong; would "report it" but cannot articulate bias mechanism or what transparency requires |
| 🟢 **3** | Rejects neutrality claim; identifies algorithmic bias from biased training data; would pause the tool; notifies candidates |
| 🔵 **4** | References Equality Act 2010 and indirect discrimination; requests vendor's fairness audit; implements human review stage; documents actions; considers ICO notification obligation |

Revised C3 score: [[ 1 / 2 / 3 / 4 ]]

</div>

---

## Deep Dive — C4: Data Protection (for any level — always probe)

<span class="tag tag-knowledge">📘 KNOWLEDGE</span> <span class="tag tag-attitude">💡 ATTITUDE</span> <span class="tag tag-individual">INDIVIDUAL</span>

<div class="individual-box">

### 📋 Decision Task — Ask the participant to respond to each

*For each action below, say whether it is: ✅ Acceptable | ⚠️ Needs policy check | ❌ Never acceptable*

| Action | Their Decision |
|---|---|
| Asking ChatGPT to help draft a generic job description | |
| Pasting 40 employees' names and salaries into ChatGPT | |
| Using Copilot (within Microsoft 365) to summarise a performance review note | |
| Uploading a disciplinary hearing transcript to a free AI summariser | |
| Using Perplexity to find public salary benchmarks | |

**Ask:** What is the difference between data you own and data about other people? Why does that matter in AI?

</div>

<div class="rubric-box">

### 🧑‍🏫 SCORING — C4 Deep Dive

**Correct answers:** Generic JD = ✅ | Salary data = ❌ | Copilot/M365 = ⚠️ (depends on tenancy settings) | Disciplinary transcript = ❌ | Public benchmarks = ✅

| Level | Response Pattern |
|---|---|
| 🔴 **1** | Selects ✅ for most; sees no risk in salary data; cannot explain the distinction |
| 🟡 **2** | Correctly identifies the obvious risks (salary, disciplinary) but unsure about Copilot |
| 🟢 **3** | All correct; explains personal data vs. public data; understands Copilot's data residency question |
| 🔵 **4** | All correct with legal reasoning; mentions GDPR lawful basis; knows to check Microsoft tenancy configuration and Data Processing Agreement |

Revised C4 score: [[ 1 / 2 / 3 / 4 ]]

</div>

---

## Deep Dive — C5: Verification (for Novice / Developing)

<span class="tag tag-skill">🔧 SKILL</span> <span class="tag tag-individual">INDIVIDUAL</span>

<div class="individual-box">

### 📋 Live Verification Task

**Give the participant this AI-generated paragraph:**

> *"According to the 2022 CIPD Future of Work Report, 78% of UK organisations now use AI tools in their HR function, and this is projected to rise to 95% by 2027."*

**Ask them to verify this claim in 5 minutes using any tools available.**

**Observe:** Do they go to the CIPD website directly? Do they use Perplexity to find the source? Do they check the actual report? Do they notice if the figure cannot be confirmed?

</div>

<div class="rubric-box">

### 🧑‍🏫 SCORING — C5 Deep Dive

| Level | Observed Behaviour |
|---|---|
| 🔴 **1** | Accepts the figure; does not attempt to verify; or only searches on Google and accepts the first result |
| 🟡 **2** | Visits CIPD website but cannot find the specific report; gives up after one attempt |
| 🟢 **3** | Navigates to cipd.co.uk; searches for the 2022 report; notes if the figure is not confirmed there; identifies potential hallucination |
| 🔵 **4** | Finds the actual CIPD source; notes the specific data does not match (hallucination); searches an alternative database; documents the discrepancy and flags it clearly |

Revised C5 score: [[ 1 / 2 / 3 / 4 ]]

</div>

--------------------------------------------------------------------------

# Phase 5: Competency Gap Mapping

<span class="time-chip">⏱ 10 minutes — Trainer Only</span>

--{{0}}--
This phase is for you alone. Consolidate all scores from Phases 2, 3, and 4 into the master matrix. This is the evidence base from which you issue every development prescription.

<div class="phase-header"><div class="phase-num">5</div><div><strong>GAP MAPPING</strong> — Consolidate all scores; identify patterns</div></div>

---

## 5.1 Master Competency Score Matrix

**Transfer your final scores here. Where a competency was assessed in multiple phases, use the highest-evidence score (typically the Phase 4 deep dive).**

[[C1: Foundations][C2: Tools][C3: Ethics][C4: Data][C5: Verification]]
[P01 – Name] Final score
[P02 – Name] Final score
[P03 – Name] Final score
[P04 – Name] Final score
[P05 – Name] Final score

---

## 5.2 Total Score Interpretation

| Total (out of 20) | Level | Required Action |
|---|---|---|
| **5 – 8** | 🔴 Novice | Urgent structured intervention — foundational AI literacy programme before independent AI use |
| **9 – 12** | 🟡 Developing | Guided learning — targeted gap-filling modules; supervised AI use in workplace |
| **13 – 16** | 🟢 Competent | Consolidation — apply in workplace with peer support; review in 4 weeks |
| **17 – 20** | 🔵 Advanced | Extended challenge — peer mentoring, policy drafting, cohort co-facilitation |

---

## 5.3 Gap Flag Decision

**Are C4 (Data Privacy) scores predominantly Level 1 across the group?**

[( )] YES — **STOP.** This is a live compliance risk. Escalate to your Data Protection Officer and L&D manager before any participant uses AI tools unsupervised. Issue an emergency C4 briefing.
[( )] NO — continue to individual prescription.

**Are C3 (Ethics) scores predominantly Level 1 across the group?**

[( )] YES — Review whether AI is currently being used in any live HR processes (recruitment screening, performance assessment). If so, pause those processes pending review.
[( )] NO — continue to individual prescription.

---

## 5.4 Individual Gap Profile

<div class="gap-box">

### ⚠️ Complete One Per Participant

**Participant ID:** [[ P01 ]]

**Name:** [[ _____ ]]

**Total Score:** [[ /20 ]]      **Overall Level:** [[ Novice / Developing / Competent / Advanced ]]

**Competency gaps identified (Level 1 or 2):**

[[ ]] C1 — AI Foundations

[[ ]] C2 — Tool Selection

[[ ]] C3 — Ethics

[[ ]] C4 — Data Protection

[[ ]] C5 — Verification

**Priority gap (lowest score):** [[ _____ ]]

**What this participant is strong in:** [[ _____ ]]

**Trainer gap summary (2–3 sentences for prescription brief):** [[ _____ ]]

</div>

--------------------------------------------------------------------------

# Phase 6: Development Prescription

<span class="time-chip">⏱ 10 minutes — Trainer Decision</span>

--{{0}}--
You now issue each participant a directed personal development plan. This is not optional — it is a structured directive with a deadline, a specific action, and an evidence requirement that you will check at the post-assessment.

<div class="phase-header"><div class="phase-num">6</div><div><strong>DEVELOPMENT PRESCRIPTION</strong> — You direct; they act</div></div>

---

## 6.1 Gap-to-Intervention Reference

| Competency Gap | Prescribed Intervention | Evidence Required from Participant |
|---|---|---|
| **C1 Level 1** | Complete Google's "Introduction to Generative AI" (Coursera, free, 45 min) | Completion screenshot + 150-word written reflection |
| **C1 Level 2** | Watch 3 specified AI explainer videos; write a 200-word summary of AI limitations | Written summary |
| **C2 Level 1** | Conduct a structured tool comparison: use ChatGPT, Consensus, and Perplexity for the same research question; document differences | Completed comparison table |
| **C2 Level 2** | Complete one real workplace task using Consensus; submit sources found | Submitted source list |
| **C3 Level 1** | Study the UNESCO AI Ethics Recommendations; complete trainer-provided bias case study analysis | Written analysis |
| **C3 Level 2** | Read ICO guidance on AI and data protection; complete one ethical decision scenario | Scenario response submitted to trainer |
| **C4 Level 1 — URGENT** | Read organisational AI & data policy within 48 hours; sign policy acknowledgement; complete ICO data protection awareness module | Signed acknowledgement + module certificate |
| **C4 Level 2** | Complete the ICO online data protection module; audit one HR process for data risk | Written risk audit |
| **C5 Level 1** | Complete a trainer-assigned fact-checking exercise: verify 5 AI claims against authoritative sources; submit verification log | Verification log |
| **C5 Level 2** | Apply verification habit to one live work task; document what the AI got right and wrong | Reflection submitted to trainer |
| **Any area Level 3** | Apply competency in a real workplace task; submit 150-word reflection to trainer | Written reflection |
| **All areas Level 4** | Co-facilitate the next cohort's assessment session under trainer supervision | Facilitation observation report |

---

## 6.2 Development Prescription Form

<div class="prescription-box">

### ✅ INDIVIDUAL DEVELOPMENT PRESCRIPTION

**Participant Name:** [[ _____ ]]     **ID:** [[ P01 ]]

**Issued by (Trainer):** [[ _____ ]]

**Date Issued:** [[ DD/MM/YYYY ]]     **Review Date:** [[ DD/MM/YYYY ]]

---

**Current Level:** [[ Novice / Developing / Competent / Advanced ]]

**Total Score:** [[ /20 ]]

**Priority Gap:** [[ C1 / C2 / C3 / C4 / C5 ]]

---

**PRESCRIBED ACTION 1 (complete by: [[ date ]])**

Task: [[ specific action — e.g., "Complete Google's Introduction to Generative AI on Coursera" ]]

Evidence to submit: [[ e.g., "Completion certificate + 150-word reflection" ]]

---

**PRESCRIBED ACTION 2 (complete by: [[ date ]])**

Task: [[ specific action ]]

Evidence to submit: [[ _____ ]]

---

**PRESCRIBED ACTION 3 (complete by: [[ date ]])**

Task: [[ specific action ]]

Evidence to submit: [[ _____ ]]

---

**Trainer's message to this participant:**

[[ Personal note — what specifically you want them to focus on and why it matters for their role ]]

</div>

---

## 6.3 Prescription Tracker — All Participants

| ID | Priority Gap | Action 1 Due | Action 2 Due | Action 3 Due | Evidence Deadline |
|---|---|---|---|---|---|
| P01 | | | | | |
| P02 | | | | | |
| P03 | | | | | |
| P04 | | | | | |
| P05 | | | | | |

--------------------------------------------------------------------------

# Phase 7: Post-Assessment and Verification

<span class="time-chip">⏱ 15 minutes — Trainer Administered</span>

--{{0}}--
Re-administer the same five task types from Phase 2 after all prescribed actions have been completed. Score fresh, using the same rubrics. The before-and-after comparison is your measurable evidence of competency development.

<div class="phase-header"><div class="phase-num">7</div><div><strong>POST-ASSESSMENT</strong> — Re-administer, re-score, verify progress</div></div>

<div class="trainer-banner">

### 🧑‍🏫 TRAINER INSTRUCTION

Do **not** remind participants of their previous answers. Score responses fresh. The chart below will display example group averages — update the data values to match your actual scores.

</div>

---

## Post-Assessment Tasks (Re-Administer to Participants)

<div class="employee-task">

### 📋 Post-Assessment Task Sheet

**P-A1.** Explain in your own words what "hallucination" means in AI and give a specific HR example of how it could cause a problem.

[[ _____ ]]

**P-A2.** Your manager asks for evidence-based research on the impact of four-day working weeks. Which tool do you choose and why?

[[ _____ ]]

**P-A3.** Name two ethical risks of using AI in performance management and explain how each should be managed.

[[ _____ ]]

**P-A4.** Give two examples of employee data that must not be entered into ChatGPT, and explain the legal reason.

[[ _____ ]]

**P-A5.** An AI tool tells you that the ACAS code of practice was updated in January 2026 to include AI-specific guidance. Describe your step-by-step process for verifying this before including it in a policy.

[[ _____ ]]

</div>

---

## Post-Assessment Score Entry

[[C1: Foundations][C2: Tools][C3: Ethics][C4: Data][C5: Verification]]
[P01 POST] Final post score
[P02 POST] Final post score
[P03 POST] Final post score
[P04 POST] Final post score
[P05 POST] Final post score

---

## Before and After — Group Progress Chart

<div class="trainer-banner">

### 📊 Group Average Competency Progress

**Update the data values in the code below to match your actual group average scores before and after. Example scores are pre-loaded.**

</div>

<div id="chart-wrap" style="background:white; border-radius:10px; padding:20px; margin:16px 0; box-shadow:0 2px 12px rgba(0,0,0,0.1);">
<canvas id="progressChart" width="640" height="340"></canvas>
</div>

<script>
(function () {
  var attempts = 0;
  function tryRender() {
    attempts++;
    var canvas = document.getElementById('progressChart');
    if (!canvas) { if (attempts < 20) setTimeout(tryRender, 400); return; }
    if (typeof Chart === 'undefined') { if (attempts < 20) setTimeout(tryRender, 400); return; }
    if (canvas._chartInstance) { canvas._chartInstance.destroy(); }

    // ── UPDATE THESE VALUES WITH YOUR REAL GROUP AVERAGES ──
    var preMeans  = [1.8, 2.0, 1.6, 1.5, 1.9];   // C1–C5 pre-assessment group averages
    var postMeans = [3.2, 3.4, 3.0, 3.3, 3.1];    // C1–C5 post-assessment group averages

    canvas._chartInstance = new Chart(canvas.getContext('2d'), {
      type: 'bar',
      data: {
        labels: ['C1: AI Foundations', 'C2: Tool Selection', 'C3: Ethics', 'C4: Data Privacy', 'C5: Verification'],
        datasets: [
          {
            label: 'Pre-Assessment Average',
            data: preMeans,
            backgroundColor: 'rgba(217, 48, 37, 0.72)',
            borderColor: '#d93025',
            borderWidth: 2,
            borderRadius: 4
          },
          {
            label: 'Post-Assessment Average',
            data: postMeans,
            backgroundColor: 'rgba(30, 142, 62, 0.72)',
            borderColor: '#1e8e3e',
            borderWidth: 2,
            borderRadius: 4
          }
        ]
      },
      options: {
        responsive: false,
        scales: {
          y: {
            beginAtZero: true,
            max: 4,
            ticks: {
              stepSize: 1,
              callback: function (val) {
                return ['', '1 Novice', '2 Developing', '3 Competent', '4 Advanced'][val] || '';
              },
              font: { size: 11 }
            },
            grid: { color: 'rgba(0,0,0,0.06)' }
          },
          x: { ticks: { font: { size: 11 } }, grid: { display: false } }
        },
        plugins: {
          legend: { position: 'top', labels: { font: { size: 12 }, padding: 16 } },
          title: {
            display: true,
            text: 'Group Competency Progress: Pre-Assessment vs Post-Assessment',
            font: { size: 14, weight: 'bold' },
            padding: { bottom: 16 }
          },
          tooltip: {
            callbacks: {
              label: function (ctx) {
                var labels = ['', 'Novice', 'Developing', 'Competent', 'Advanced'];
                var v = ctx.parsed.y;
                return ctx.dataset.label + ': ' + v.toFixed(1) + ' (' + (labels[Math.round(v)] || '') + ')';
              }
            }
          }
        }
      }
    });
  }
  setTimeout(tryRender, 600);
})();
</script>

---

## Individual Before & After Verification Table

| Participant | Pre Total /20 | Post Total /20 | Score Change | Gap Status |
|---|---|---|---|---|
| P01 | | | | ✅ / ⚠️ / ❌ |
| P02 | | | | ✅ / ⚠️ / ❌ |
| P03 | | | | ✅ / ⚠️ / ❌ |
| P04 | | | | ✅ / ⚠️ / ❌ |
| P05 | | | | ✅ / ⚠️ / ❌ |

**Gap Status Key:**

- ✅ **Closed** — Improved by 2+ points across all gap areas → Issue competency acknowledgement
- ⚠️ **Partially Closed** — Improved by 1 point → Issue revised prescription; re-assess in 2 weeks
- ❌ **Persists** — No improvement or decline → Escalate to L&D manager; mandatory structured intervention

---

## Trainer Outcome Decision

| Outcome | Criteria | Your Next Action |
|---|---|---|
| ✅ **Competency Achieved** | Score ≥ 14/20 AND all individual areas ≥ Level 3 | Issue completion acknowledgement; assign peer mentoring or advanced challenge |
| ⚠️ **Further Development** | Score 9–13 OR one area remains Level 1–2 | Revised prescription; 2-week review scheduled |
| ❌ **Structured Intervention** | Score ≤ 8 OR C4 Data Privacy remains Level 1 | Do not permit unsupervised AI use; escalate to L&D and DPO |

**Record outcome per participant:**

P01: [[ Achieved / Further Development / Structured Intervention ]]

P02: [[ Achieved / Further Development / Structured Intervention ]]

P03: [[ Achieved / Further Development / Structured Intervention ]]

P04: [[ Achieved / Further Development / Structured Intervention ]]

P05: [[ Achieved / Further Development / Structured Intervention ]]

--------------------------------------------------------------------------

# Trainer Reference and Resources

--{{0}}--
This final section gives you everything you need to run the programme consistently across multiple cohorts — a quick rubric reference, data protection red lines, and a full session evidence checklist.

## AI Tool Quick Reference

| Tool | URL | Designed For | Recommend When |
|---|---|---|---|
| **ChatGPT** | chat.openai.com | Drafting, ideas, summarising | First drafts; no evidence required |
| **Consensus** | consensus.app | Peer-reviewed evidence with citations | Policy work; research credibility required |
| **Copilot** | copilot.microsoft.com | Microsoft 365 productivity | Documents, data, meetings within M365 |
| **Perplexity AI** | perplexity.ai | Sourced web search | Quick factual lookups with linked sources |

## Data Red Lines — Never Acceptable in Public AI Tools

<div class="gap-box">

<h4>🔴 These must be communicated as absolute prohibitions</h4>

- Employee names combined with any personal attribute (salary, performance, health, disciplinary)
- Grievance, disciplinary, or investigation records
- Recruitment application data
- Medical, occupational health, or mental health information
- Any GDPR Article 9 special category data
- Trade union membership information
- Financial account or payroll data

</div>

## Ethical Principles — Reinforce in Every Session

<div class="tip-box">

1. **Human oversight** — AI supports decisions; humans remain accountable for outcomes
2. **Bias awareness** — AI reflects and can amplify biases in its training data
3. **Transparency** — People affected by AI-influenced decisions must be told
4. **Privacy** — Confidential and personal data must not enter public AI tools
5. **Verification** — All AI outputs must be checked against authoritative sources before use in professional work

</div>

## End-of-Session Evidence Pack Checklist

<ul class="checklist">
<li>Participant register completed with names, roles, and IDs</li>
<li>All Phase 2 task sheets scored and filed</li>
<li>Phase 3 group observation records completed per participant</li>
<li>Phase 4 deep-dive scores recorded per individual</li>
<li>Master competency matrix (Phase 5) completed</li>
<li>Individual gap profiles written (Phase 5)</li>
<li>Development prescriptions issued to every participant (Phase 6)</li>
<li>Prescription tracker completed and stored (Phase 6)</li>
<li>Post-assessment task sheets scored (Phase 7)</li>
<li>Before-and-after comparison table completed (Phase 7)</li>
<li>Outcome decision recorded for every participant (Phase 7)</li>
<li>Any C4/C3 compliance escalations raised and documented</li>
<li>Before-and-after chart updated with actual group scores</li>
</ul>

---

## References

UNESCO. (2022). *Recommendation on the ethics of artificial intelligence.* UNESCO. https://unesdoc.unesco.org/ark:/48223/pf0000381137

UNESCO. (2024). *AI competency framework for teachers and students.* UNESCO.

Information Commissioner's Office. (2023). *Guidance on AI and data protection.* ICO. https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/artificial-intelligence/

Knowles, M. S., Holton, E. F., & Swanson, R. A. (2020). *The adult learner: The definitive classic in adult education and human resource development* (9th ed.). Routledge.

OECD. (2024). *OECD AI principles.* OECD. https://www.oecd.org/digital/artificial-intelligence/

Consensus AI. (2025). *Evidence synthesis and citation-based AI search platform.* https://consensus.app

---

<div class="trainer-banner">

### 🧑‍🏫 Programme Complete

This assessment programme produces a fully evidenced competency record for every participant: observed pre-score, identified gaps, directed intervention, and verified post-score. That evidence constitutes the **AI Competency Development Portfolio** for each individual and your team as a whole.

</div>
